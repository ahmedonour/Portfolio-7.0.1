<script>
	import Circles from '../components/Home/Circles.svelte';
	import HeroText from '../components/Home/HeroText.svelte';
</script>

<main>
    <HeroText />
	<Circles />
</main>

<style>
	main {
		width: 100vw;
		height: calc(100vh - 90px);
		background-color: var(--clr-SkyBlue);
		display: grid;
		place-items: center;
	}
</style>
