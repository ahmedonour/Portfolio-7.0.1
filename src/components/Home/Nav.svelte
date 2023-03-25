<script>
	import { fade, fly } from 'svelte/transition';
	import { onMount } from 'svelte';
	var visible = true;
	function toggleVisible() {
		visible = !visible;
	}
</script>

<svelte:head>
	<script src="https://kit.fontawesome.com/f3c7bd6f07.js" crossorigin="anonymous"></script>
</svelte:head>
<main>
	<nav>
		<h1><a href="/">AS</a></h1>
		<button on:click={toggleVisible}>
			<svg viewBox="0 0 100 80" width="40" height="40">
				<rect width="100" height="20" rx="10" />
				<rect y="30" width="50" height="20" rx="10" />
				<rect y="60" width="100" height="20" rx="10" />
			</svg>
		</button>
		{#if !visible}
			<ul in:fly={{ x: 100, duration: 500 }} out:fly={{ x: -100, duration: 500 }}>
				<button on:click={toggleVisible}><i class="fas fa-times" /></button>
				<div class="left-side">
					<li><a href="/" on:click={toggleVisible}>Home</a></li>
					<li><a href="/about" on:click={toggleVisible}>About</a></li>
					<li><a href="/work" on:click={toggleVisible}>Work</a></li>
				</div>
				<li><a href="mailto:ahmedonour.49@gmail.com" on:click={toggleVisible}>Let's Talk</a></li>
			</ul>
		{/if}
	</nav>
</main>

<style>
	main {
		width: 100vw;
		display: grid;
		place-items: center;
	}
	nav {
		display: flex;
		width: 80vw;
		height: 100px;
		justify-content: space-between;
		align-items: center;
	}
	nav a {
		text-decoration: none;
		color: var(--clr-Black);
	}
	nav h1 {
		font-family: var(--ff-sec);
		font-size: 3rem;
	}
	nav ul {
		width: 100vw;
		height: calc(100vh - 100px);
		position: absolute;
		top: 100px;
		left: 0;
		padding-left: 8rem;
		background-color: rgba(255, 255, 255, 0.219);
		list-style: decimal-leading-zero;
		font-size: 3rem;
		font-family: var(--ff-main);
		backdrop-filter: blur(10px);
		-webkit-backdrop-filter: blur(10px);
		z-index: 99999;
	}
	nav ul li {
		font-weight: 800;
	}
	nav button {
		background: none;
		border: none;
		font-size: 2rem;
	}
	.fa-times {
		position: relative;
		/* bottom :20px; */
		left: -100px;
		padding: 0.6rem 1rem;
		border-radius: 50px;
		border: 1px solid #000;
	}
	@media screen and (min-width: 768px) {
		main {
			display: none;
		}
	}
</style>
