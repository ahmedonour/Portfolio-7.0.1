<script>
	import { fade } from 'svelte/transition';
	let visible = true;
</script>

<main>
	<h1 transition:fade>Ahmed Suliman</h1>
	<p>Front-End Developer & Designer</p>
	<p>
		I deliver stunning and engaging websites that captivate audiences and elevate online presence by
		leveraging the latest technologies and best practices
	</p>
</main>

<style>
	main {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		position: fixed;
		z-index: 999;
		color: var(--clr-Black);
	}
	main h1 {
		font-family: var(--ff-main);
		font-size: 8rem;
	}
	main p {
		font-weight: 700;
		font-family: var(--ff-main);
	}
	main p:nth-of-type(1) {
		font-size: 2.5rem;
		letter-spacing: 10px;
	}
	main p:nth-of-type(2) {
		font-size: 1.5rem;
		text-align: justify;
		width: 60%;
	}
</style>
