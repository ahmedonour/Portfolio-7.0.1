<script>
	import { fly } from 'svelte/transition';
	import SocialIcons from '../../components/socialIcons.svelte';
	import UniText from '../../components/uni-text.svelte';
	let Class = 'about-section';
</script>

<svelte:head>
	<title>Ahmed Suliman | About me</title>
	<script src="https://kit.fontawesome.com/f3c7bd6f07.js" crossorigin="anonymous"></script>
</svelte:head>
<main
	in:fly={{ y: 200, duration: 300, delay: 500 }}
	out:fly={{ y: 200, duration: 300, delay: 500 }}
>
	<!-- <div class="about_section">
		<h1>About</h1>
		<p>
			As a front end developer, my goal is to create stunning and engaging websites that will
			capture the attention of your audience and leave a lasting impression. With my expertise in
			website design and development, I specialize in creating custom social media influencer
			portfolios that showcase your brand and personality.
		</p>
	</div> -->
	<div class="me">
		<UniText
			myClass="about-section"
			myH1="About"
			myP="As a front end developer, my goal is to create stunning and engaging websites that will
		capture the attention of your audience and leave a lasting impression. With my expertise in
		website design and development, I specialize in creating custom social media influencer
		portfolios that showcase your brand and personality."
		/>
	</div>
	<div class="me">
		<h1>About Me</h1>
		<div class="me_img">
			<img src="me3.png" alt="" srcset="" />
			<p>
				Meet Ahmed Suliman, a passionate Front-End developer who loves to learn and grow every day.
				He has a keen interest in reading and writing, and always looks forward to exploring new
				things. When he's not coding, you'll find him indulging in his love for sports. With an eye
				for detail and a hunger for knowledge, Ahmed is always ready to take on new challenges and
				bring his unique perspective to every project he works on.
			</p>
		</div>
	</div>

	<SocialIcons title="Follow Me" />
</main>

<style>
	main {
		width: var(--width-Scroll);
		display: grid;
		place-items: center;
	}

	.me {
		margin: 1rem;
		width: 78%;
	}
	.me h1 {
		font-family: var(--ff-main);
		font-size: 3rem;
		color: var(--clr-Black);
	}
	.me .me_img {
		display: flex;
		flex-direction: column;
	}
	.me .me_img img {
		border-radius: 50%;
		width: 100%;
		margin-bottom: 1rem;
		filter: saturate(0);
	}
	.me .me_img p {
		font-family: var(--ff-p);
		font-weight: 500;
		text-align: justify;
		font-size: 1rem;
		letter-spacing: 1px;
		line-height: 1.5;
		color: var(--clr-Black);
	}

	@media screen and (min-width: 1024px) {
		.me .me_img {
			flex-direction: row;
			justify-content: center;
			align-items: center;
		}
		.me h1 {
			font-size: 8rem;
		}
		.me .me_img p {
			font-size: 1.8rem;
			font-weight: 800;
			text-align: justify;
		}
	}
</style>
