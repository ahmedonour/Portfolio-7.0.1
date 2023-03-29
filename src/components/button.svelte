<script>
	function toggle() {
		window.document.body.classList.toggle('dark-mode');
	}
</script>

<button on:click={toggle}>
	<slot />
</button>

<style>
	button {
		background-color: transparent;
		color: var(--clr-Black);
		border: none;
		border-radius: 4px;
		padding: 0.5rem;
		text-transform: uppercase;
		font-family: var(--ff-p);
		font-size: 2rem;
		font-weight: 700;
	}
	:global(body.dark-mode) button {
		/* background-color: #0084f6;
            color: white; */
		/* --clr-Black: #ffffff;
		--clr-SkyBlue: #222222; */
	}
</style>
