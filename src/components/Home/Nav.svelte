<nav>
	<h1>AS</h1>
	<ul>
		<li>Let's Talk</li>
		<div class="left-side">
			<li>About</li>
			<li>Work</li>
		</div>
	</ul>
</nav>

<style>
	nav {
		width: 100vw;
		height: 90px;
		display: flex;
		justify-content: space-around;
		align-items: center;
		background-color: var(--clr-SkyBlue);
	}
	nav h1 {
		font-family: var(--ff-sec);
		font-size: 4rem;
		color: var(--clr-Black);
	}
	nav ul {
		font-family: var(--ff-main);
		list-style: none;
		width: 50%;
		font-size: 1.3rem;
		font-weight: 700;
		display: flex;
		justify-content: space-between;
		align-items: center;
		color: var(--clr-Black);
	}
	nav ul .left-side {
		display: flex;
		justify-content: space-around;
		width: 50%;
	}
</style>
