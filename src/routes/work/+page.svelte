<script>
	import { fly } from 'svelte/transition';
	import LinkProjects from '../../components/projects/linkProjects.svelte';
	import Tools from '../../components/projects/tools.svelte';
	import UniText from '../../components/uni-text.svelte';
</script>

<svelte:head>
	<title>Ahmed Suliman | My work</title>
</svelte:head>
<main
	in:fly={{ y: 200, duration: 500, delay: 300 }}
	out:fly={{ y: 200, duration: 500, delay: 300 }}
>
	<div class="me">
		<h1>Work</h1>
		<!-- <UniText myH1="Work" myP="My Favorite projects" /> -->
		<section>
			<LinkProjects titleOfUri="OnourAi" uri="work/onourai" />
			<LinkProjects titleOfUri="News" uri="work/newsHomepage" />
			<LinkProjects titleOfUri="ToDo" uri="work/todo" />
		</section>
		<h1>Other Projects</h1>
		<!-- <UniText myH1="Other Projects" myP="In my GitHub" /> -->
		<section class="github">
			<a href="https://github.com/ahmedonour/"><i class="fab fa-github" /></a>
		</section>
	</div>
</main>

<style>
	main {
		width: var(--width-Scroll);
		display: grid;
		place-items: center;
	}
	h1{
		font-size: 3rem;
		color: var(--clr-Black);
		font-family: var(--ff-main);
	}
	.fa-github {
		color: var(--clr-Black);
		margin-top: 2rem;
		font-size: 10rem;
	}
	.github {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		width: 78%;
	}
	@media only screen and (min-width: 1024px) {
		section {
			display: flex;
			flex-direction: column;
			justify-content: center;
			align-items: flex-start;
			width: 78%;
		}
		h1{
		font-size: 8rem;
		color: var(--clr-Black);
		font-family: var(--ff-main);
	}
	}
</style>
