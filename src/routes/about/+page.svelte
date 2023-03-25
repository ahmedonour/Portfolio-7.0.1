<script>
</script>

<svelte:head>
	<title>Ahmed Suliman | About me</title>
    <script src="https://kit.fontawesome.com/f3c7bd6f07.js" crossorigin="anonymous"></script>
</svelte:head>
<main>
<div class="about_section">
    <h1>About</h1>
    <p>As a front end developer, my goal is to create stunning and engaging websites that will capture the attention of your audience and leave a lasting impression. With my expertise in website design and development, I specialize in creating custom social media influencer portfolios that showcase your brand and personality.
</div>
<div class="me">
    <h1>About Me</h1>
    <div class="me_img">
        <img src="me3.png" alt="" srcset="">
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Fugit repellat dolorum corporis molestiae repellendus, ad accusamus, exercitationem voluptas ab maiores eos omnis maxime expedita error animi ut dicta delectus deserunt!</p>
    </div>
</div>
<div class="social">

</div>
</main>

<style>
    main{
        width: 100vw;
        display: grid;
        place-items: center;
    }
    .about_section{
        width: 78%;
        font-family: var(--ff-main);
        font-size: 3rem;
    }   
    .about_section p{
        font-family: var(--ff-p);
        font-weight: 500;
        text-align: justify;
        font-size:  1.5rem;
        letter-spacing: 1px;
        line-height: 1.5;
    }
    .me{
        margin: 1rem;
        width: 78%;
    }
    .me h1{
        font-family: var(--ff-main);
        font-size: 3rem;
    }
    .me .me_img{
        display: flex;
        flex-direction: column;
    }
    .me .me_img img{
        
        width: 100%;
    }
    .me .me_img p{
        font-family: var(--ff-p);
        font-weight: 500;
        text-align: justify;
        font-size:  1rem;
        letter-spacing: 1px;
        line-height: 1.5;
    }
</style>
