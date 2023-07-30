<script>
	import Circles from '../components/Home/Circles.svelte';
	import HeroText from '../components/Home/HeroText.svelte';
	import SocialIcons from '../components/socialIcons.svelte';
</script>

<svelte:head>
	<title>Ahmed Suliman | Front-End Developer & Designer</title>
</svelte:head>
<main>
	<HeroText />
	<Circles />
</main>

<style>
	main {
		width: var(--width-Scroll);
		height: calc(100vh - 90px);
		background-color: var(--clr-SkyBlue);
		display: grid;
		place-items: center;
	}
</style>
