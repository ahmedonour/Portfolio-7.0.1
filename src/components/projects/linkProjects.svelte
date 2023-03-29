<script>
	export let uri;
	export let titleOfUri;
</script>

<div>
	<h1><a href={uri}>{titleOfUri}</a></h1>
</div>

<style>
	h1 {
		--width: auto;
		width: var(--width);
		font-size: 20vw;
		font-family: var(--ff-main);
		font-weight: 800;
	}
	h1 a {
		color: var(--clr-Black);
	}
</style>
