<script>
	export let title;
	import { fly } from 'svelte/transition';
</script>

<div
	class="social"
	in:fly={{ y: 200, duration: 1400, delay: 900 }}
	out:fly={{ y: 200, duration: 1400, delay: 900 }}
>
	<h1>{title}</h1>
	<div class="icons">
		<a href="https://web.facebook.com/OnodevDeveloper"><i class="fab fa-facebook" /></a>
		<a href="https://dev.to/ahmed_onour"><i class="fab fa-dev" /></a>
		<a href="https://medium.com/@ahmedsuliman/"><i class="fab fa-medium" /></a>
		<a href="https://twitter.com/ahmed_onour"><i class="fab fa-twitter" /></a>
		<a href="https://blog.ahmedsuliman.com/"><i class="fab fa-hashnode" /></a>
	</div>
</div>

<style>
	.social {
		width: 78%;
		padding-bottom: 2rem;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
	}
	.social h1 {
		font-family: var(--ff-main);
		font-size: 3rem;
		color: var(--clr-Black);
	}
	.social a {
		color: var(--clr-Black);
		font-size: 2rem;
		margin-left: 1rem;
	}
	@media only screen and (min-width: 1024px) {
		.social {
			display: flex;
			flex-direction: column;
			justify-content: center;
			align-items: center;
		}
	}
</style>
