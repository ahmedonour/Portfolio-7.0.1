<script>
	import { fly } from 'svelte/transition';
	import UniText from '../../components/uni-text.svelte';
</script>

<svelte:head>
	<title>Ahmed Suliman | My work</title>
</svelte:head>
<main
	in:fly={{ y: 200, duration: 500, delay: 300 }}
	out:fly={{ y: 200, duration: 500, delay: 300 }}
>
	<UniText myH1="Work" myP="This is Hand picked Projects" />
</main>

<style>
	main {
		width: var(--width-Scroll);
		display: grid;
		place-items: center;
	}
</style>
