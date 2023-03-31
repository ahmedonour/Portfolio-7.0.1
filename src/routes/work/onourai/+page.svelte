<script>
	import BackButton from "../../../components/projects/backButton.svelte";
	import ImageAndDes from "../../../components/projects/imageAndDes.svelte";
    import ImageSlider from "../../../components/projects/imageSlider.svelte";
    import UniText from "../../../components/uni-text.svelte";
    import Tools from "../../../components/projects/tools.svelte";
    let image = [
        "/onourai/img1.png",
        "/onourai/img2.png",
        "/onourai/img3.png",
        "/onourai/img4.png",
        "/onourai/img5.png",
        "/onourai/img6.png",
        "/onourai/img7.png",
        "/onourai/img8.png",
        "/onourai/img9.png",
        "/onourai/img10.png",
    ]

</script>
<svelte:head>
    <title>My Projects | OnourAI</title>
  </svelte:head>
<main>
    <section>
        <BackButton />
        <div class="image">
            <!-- svelte-ignore a11y-missing-attribute -->
            <ImageSlider images={image}/>
            <UniText 
            myH1="OnourAi"
            myP=" OnourAi is an Arabic AI Image Generator that utilizes the SvelteKit framework, the OpenAI API, and a translating API to generate images based on user inputs. The goal of this project is to provide an easy-to-use tool for users to create customized images in the Arabic language, even if they are not fluent in Arabic themselves. The AI algorithms will generate images based on user-provided input and translate the generated text into English for the final output."
            />
            <div class="links">
                <a href="https://github.com/ahmedonour/Image-Generator-SvelteKit" target="_blank"><i class="fab fa-github"/></a>
                <a href="https://onodevai.netlify.app/" target="_blank"><i class="fas fa-globe"/></a>
            </div>
            <h1>Tools</h1>
            <div class="tools">
                <Tools toolName='Figma' />
                <Tools toolName='SvelteKit' />
                <Tools toolName='OpenAI' />
                <Tools toolName='TranslateAI' />
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
    }
    .links{
        width: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
    }
    .links a{
        color: var(--clr-Black);
        padding-left: 5rem;
        font-size: 4rem;
        transition: all .5s ease-in-out;
    }
    .links a:hover{

        font-size: 5rem
    }
    @media only screen and (min-width: 1024px){
        .tools{
            flex-wrap: nowrap;
            gap: 5rem;
        }
    }
</style>