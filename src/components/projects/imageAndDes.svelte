<script>
	import UniText from "../uni-text.svelte";
import BackButton from "./backButton.svelte";
	import ImageSlider from "./imageSlider.svelte";
    // export let imgSrc;
    let image = ["/show1.png", "/show2.png"]

</script>
<section>
    <BackButton />
    <div class="image">
        <!-- svelte-ignore a11y-missing-attribute -->
        <ImageSlider images={image}/>
        <UniText 
        myH1="OnourAi :"
        myP=" OnourAi is an Arabic AI Image Generator that utilizes the SvelteKit framework, the OpenAI API, and a translating API to generate images based on user inputs. The goal of this project is to provide an easy-to-use tool for users to create customized images in the Arabic language, even if they are not fluent in Arabic themselves. The AI algorithms will generate images based on user-provided input and translate the generated text into English for the final output."
        />
    </div>
</section>
<style>
    section{
        width: 80%;
    }
    section 
    section .image {
        width: 100%;
    }
    section .image img{
        width: 100%;
        border-radius: 2rem;
    }
</style>