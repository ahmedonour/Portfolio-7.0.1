<script>
	import BackButton from "../../../components/projects/backButton.svelte";
	import ImageAndDes from "../../../components/projects/imageAndDes.svelte";
    import ImageSlider from "../../../components/projects/imageSlider.svelte";
    import UniText from "../../../components/uni-text.svelte";
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
            myH1="OnourAi :"
            myP=" OnourAi is an Arabic AI Image Generator that utilizes the SvelteKit framework, the OpenAI API, and a translating API to generate images based on user inputs. The goal of this project is to provide an easy-to-use tool for users to create customized images in the Arabic language, even if they are not fluent in Arabic themselves. The AI algorithms will generate images based on user-provided input and translate the generated text into English for the final output."
            />
            <!-- <Tools /> -->
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
</style>