<script>
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