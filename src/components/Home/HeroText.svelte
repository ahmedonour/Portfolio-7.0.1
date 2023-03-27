<script>
	import { fly } from 'svelte/transition';
</script>

<main>
	<h1
		in:fly={{ y: 200, duration: 1500, delay: 1500 }}
		out:fly={{ y: 200, duration: 1500, delay: 1500 }}
	>
		Ahmed Suliman
	</h1>
	<p
		in:fly={{ y: 200, duration: 1500, delay: 1500 }}
		out:fly={{ y: 200, duration: 1500, delay: 1500 }}
	>
		Front-End Developer & Designer
	</p>
	<p
		in:fly={{ y: 200, duration: 1500, delay: 1500 }}
		out:fly={{ y: 200, duration: 1500, delay: 1500 }}
	>
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
		position: absolute;
		top: 150px;
		z-index: 999;
		color: var(--clr-Black);
		font-family: var(--ff-main);
	}
	main h1 {
		font-size: 3rem;
	}
	main p {
		font-weight: 700;
	}
	main p:nth-of-type(1) {
		font-size: 1.2rem;
		letter-spacing: 2px;
		font-weight: 800;
	}
	main p:nth-of-type(2) {
		font-size: 1rem;
		text-align: justify;
		width: 80%;
		font-weight: 400;
		font-family: var(--ff-p);
	}
	@media screen and (min-width: 1024px) {
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
			width: 50%;
			font-weight: 500;
		}
	}
</style>
