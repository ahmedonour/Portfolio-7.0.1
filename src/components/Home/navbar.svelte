<script>
	import { fade, fly } from 'svelte/transition';
	import { onMount } from 'svelte';
	var visible = true;
	function toggleVisible() {
		visible = !visible;
	}
	onMount(async () => {
		// Add an event listener to the window's resize event
		window.addEventListener('resize', () => {
			// Check if the window width is greater than or equal to 768 pixels
			if (window.innerWidth >= 768) {
				// Set visible to false
				visible = false;
			}
		});
	});
</script>

<main>
	<nav>
		<h1><a href="/">AS</a></h1>

		<ul in:fly={{ x: 5 }} out:fly={{ x: -100, duration: 500 }}>
			<div class="left-side">
				<li><a href="/" on:click={toggleVisible}>Home</a></li>
				<li><a href="/about" on:click={toggleVisible}>About</a></li>
				<li><a href="/work" on:click={toggleVisible}>Work</a></li>
			</div>
			<li><a href="mailto:ahmedonour.49@gmail.com" on:click={toggleVisible}>Let's Talk</a></li>
		</ul>
	</nav>
</main>

<style>
	nav {
		width: 100vw;
		height: 90px;
		display: flex;
		justify-content: space-around;
		align-items: center;
		background-color: var(--clr-SkyBlue);
	}
	nav h1 {
		font-family: var(--ff-sec);
		font-size: 4rem;
		color: var(--clr-Black);
	}
	nav a {
		text-decoration: none;
		color: var(--clr-Black);
	}
	nav ul {
		position: static;
		top: 0;
		left: 0;
		padding: 0rem;
		font-family: var(--ff-main);
		list-style: none;
		width: 50%;
		font-size: 1.3rem;
		font-weight: 700;
		display: flex;
		justify-content: space-between;
		align-items: center;
		color: var(--clr-Black);
	}
	/* nav button {
			display: none;
		} */
	nav ul .left-side {
		display: flex;
		justify-content: space-around;
		width: 50%;
	}
	@media screen and (max-width: 1024px) {
		main {
			display: none;
		}
	}
</style>
