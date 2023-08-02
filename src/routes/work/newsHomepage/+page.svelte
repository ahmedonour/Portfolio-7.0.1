<script>
	import BackButton from "../../../components/projects/backButton.svelte";
	import ImageAndDes from "../../../components/projects/imageAndDes.svelte";
    import ImageSlider from "../../../components/projects/imageSlider.svelte";
    import UniText from "../../../components/uni-text.svelte";
    import Tools from "../../../components/projects/tools.svelte";
    let image = [
        "/Homepage Design/1.png",
        "/Homepage Design/2.png",
    ]

</script>
<svelte:head>
    <title>My Projects | NewsLetter Homepage</title>
  </svelte:head>
<main>
    <section>
        <BackButton />
        <div class="image">
            <!-- svelte-ignore a11y-missing-attribute -->
            <ImageSlider images={image}/>
            <UniText 
            myH1="Newsletter Homepage"
            myP="The Newsletter Homepage project is a Frontend Mentor challenge that requires building a responsive web page that displays a newsletter sign-up form with a success message."
            />
            <div class="links">
                <a href="https://github.com/ahmedonour/News-Homepage" target="_blank"><i class="fab fa-github"/></a>
                <a href="https://newsletterhomepage.netlify.app/" target="_blank"><i class="fas fa-globe"/></a>
            </div>
            <h1>Tools</h1>
            <div class="tools">
                <Tools toolName='FrontEnd mentor' />
                <Tools toolName='SvelteKit' />
                <Tools toolName='Svelte' />
                <Tools toolName='Javascript' />
            </div>
        </div>
    </section>
</main>
<style>
    section{
        width: 80%;
    }
    section .image {
        width: 100%;
    }
    main{
        width: calc(100vw -.5em);
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }
    .image h1{
        font-size: 4rem;
        color: var(--clr-Black);
        font-family: var(--ff-main);
    }
    .tools{
        /* width: 10%; */
        display: flex;
		flex-direction: row;
		justify-content: center;
		align-items: center;
        flex-wrap: wrap;
        gap: 1rem;
        margin-bottom: 5rem;
    }
    .links{
        width: 100%;
        display: flex;
        justify-content: center;
        align-items: center;

        gap: 5rem;
    }
    .links a{
        color: var(--clr-Black);
        /* padding-left: 5rem; */
        font-size: 4rem;
        transition: all .5s ease-in-out;
    }
    .links a:hover{

        font-size: 5rem
    }
    @media only screen and (min-width: 1024px){
        .tools{
            flex-wrap: nowrap;
        }
    }
</style>