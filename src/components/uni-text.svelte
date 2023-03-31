<script>
	export let myClass;
	export let myH1;
	export let myP;
</script>

<div class={myClass}>
	<h1>{myH1}</h1>
	<p>
		{myP}
	</p>
</div>

<style>
	div {
		width: 100%;
		font-family: var(--ff-main);
		font-size: 3rem;
	}
	div h1 {
		font-size: 2.5rem;
		color: var(--clr-Black);
	}
	div p {
		font-family: var(--ff-p);
		color: var(--clr-Black);

		font-weight: 500;
		text-align: justify;
		font-size: 1rem;
		letter-spacing: 1px;
		line-height: 1.5;
	}
	@media only screen and (min-width: 1024px) {
		div h1 {
			font-size: 8rem;
		}
		div p {
			font-size: 2rem;
			text-align: justify;
			font-weight: 500;
			
		}
	}
</style>
