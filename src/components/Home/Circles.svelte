<script>
</script>

<main>
	<!-- <img src="./Ellipse-1.svg" alt="" srcset="">
    <img src="./Ellipse-2.svg" alt="" srcset="">
    <img src="./Ellipse-3.svg" alt="" srcset=""> -->
	<div class="circle-1" />
	<div class="circle-2" />
	<div class="circle-3" />
</main>

<style>
	main {
		width: 90vw;
		height: 100%;
		margin: 0;
		padding: 0;
		display: grid;
		place-items: center;
		position: relative;
		/* z-index: -1; */
		overflow: hidden;
	}
	.circle-1,
	.circle-2,
	.circle-3 {
		position: absolute;
		top: 50px;
		width: 100%;
		height: 100px; /* Adjust this height according to your needs */
		border-radius: 50%;
	}
	.circle-1 {
		width: 90vw;
		height: 90vw;
		background: var(--clr-Blue);
		box-shadow: inset 0px 32px 28px rgba(0, 0, 0, 0.25);
		border-radius: 100rem;
	}
	.circle-2 {
		/* position: absolute; */
		top: 30%;
		width: 70vw;
		height: 70vw;
		background: var(--clr-Blue);
		box-shadow: inset 0px 32px 28px rgba(0, 0, 0, 0.5);
		border-radius: 100rem;
		overflow: hidden;
	}
	.circle-3 {
		/* position: absolute; */
		top: 50%;
		width: 50vw;
		height: 50vw;
		background: var(--clr-Blue);
		box-shadow: inset 0px 32px 28px rgba(0, 0, 0, 0.7);
		border-radius: 100rem;
		overflow: hidden;
	}
</style>
