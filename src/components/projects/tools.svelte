<script>
	export let toolName;
</script>

<div class="tool">
	<p>{toolName}</p>
</div>

<style>
	.tool {
		padding: 0.5rem 1.5rem;
		background-color: var(--clr-Blue);
		color: var(--clr-White);
		font-family: var(--ff-p);
		font-weight: 800;
		border-radius: 0.5rem;
		width: 90%;
		display: flex;
		flex-direction: row;
		justify-content: center;
		align-items: center;
		/* margin: 1rem; */
	}
</style>
