<script>
	import { fade, fly } from 'svelte/transition';
	import { onMount } from 'svelte';
	import Button from '../button.svelte';
	var visible = false;
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

		<ul
			class:open={visible}
			in:fly={{ x: 100, duration: 500 }}
			out:fly={{ x: -100, duration: 500 }}
		>
			<button on:click={toggleVisible}><i class="fas fa-times" /></button>

			<!-- svelte-ignore a11y-click-events-have-key-events -->
			<li on:click={() => (visible = false)}><a href="/" class:open={visible}>Home</a></li>
			<!-- svelte-ignore a11y-click-events-have-key-events -->
			<li on:click={() => (visible = false)}><a href="/about" class:open={visible}>About</a></li>
			<!-- svelte-ignore a11y-click-events-have-key-events -->
			<li on:click={() => (visible = false)}><a href="/work" class:open={visible}>Work</a></li>
			<!-- svelte-ignore a11y-click-events-have-key-events -->
			<li on:click={() => (visible = false)}>
				<a href="mailto:ahmedonour.49@gmail.com">Let's Talk</a>
			</li>
			<Button>
				<i class="fas fa-sun" />
				<i class="fas fa-moon" />
			</Button>
		</ul>
	</nav>
</main>

<style>
	:global(body.dark-mode) {
		--clr-Black: #fff;
		--clr-SkyBlue: #222222;
		--clr-Blue: #09272b;
	}
	:global(body.dark-mode) .fa-sun {
		display: block;
	}
	:global(body.dark-mode) .fa-moon {
		display: none;
	}
	.fa-sun {
		display: none;
	}
	.fas{
		cursor: pointer;
	}
	main {
		width: var(--width-Scroll);
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
		display: none;
	}
	nav ul.open {
		display: block;
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
	@media screen and (min-width: 1024px) {
		nav {
			width: 80vw;
			justify-content: space-between;
		}
		nav button {
			display: none;
		}
		nav ul {
			display: flex;
			position: relative;
			width: 40vw;
			flex-direction: row;
			justify-content: space-between;
			align-items: center;
			list-style: decimal-leading-zero;
			font-size: 1.5rem;
			font-family: var(--ff-main);
		}

		/* nav ul .left-side {
			display: flex;
			justify-content: space-between;
			align-items: center;
			width: 50%;
			margin-right: 3rem;
		} */
		nav ul li::after {
			display: block;
			content: '';
			width: 100%;
			transform: scaleX(0);
			height: 2px;
			background-color: var(--clr-Black);
			transform-origin: bottom right;
			transition: transform 0.25s ease-out;
		}
		nav ul li:hover::after {
			transform: scaleX(1);
			transform-origin: bottom left;
		}
	}
</style>
