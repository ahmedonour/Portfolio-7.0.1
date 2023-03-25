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
        <p>Meet Ahmed Suliman, a passionate Front-End developer who loves to learn and grow every day. He has a keen interest in reading and writing, and always looks forward to exploring new things. When he's not coding, you'll find him indulging in his love for sports. With an eye for detail and a hunger for knowledge, Ahmed is always ready to take on new challenges and bring his unique perspective to every project he works on.</p>
    </div>
</div>
<div class="social">
    <h1>Follow Me</h1>
    <div class="icons">
        <a href="https://web.facebook.com/OnodevDeveloper"><i class="fab fa-facebook"></i></a>
        <a href="https://dev.to/ahmed_onour"><i class="fab fa-dev"></i></a>
        <a href="https://medium.com/@ahmedsuliman/"><i class="fab fa-medium"></i></a>
        <a href="https://twitter.com/ahmed_onour"><i class="fab fa-twitter"></i></a>
        <a href="https://blog.ahmedsuliman.com/"><i class="fab fa-hashnode"></i></a>
    </div>
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
    .about_section h1{
        font-size: 3rem;
    }
    .about_section p{
        font-family: var(--ff-p);
        font-weight: 500;
        text-align: justify;
        font-size:  1rem;
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
        border-radius: 50%;
        width: 100%;
        margin-bottom: 1rem;
        filter: saturate(0);
    }
    .me .me_img p{
        font-family: var(--ff-p);
        font-weight: 500;
        text-align: justify;
        font-size:  1rem;
        letter-spacing: 1px;
        line-height: 1.5;
    }

    .social{
        width: 78%;
        padding-bottom: 2rem;
    }
    .social h1{

        font-family: var(--ff-main);
        font-size: 4rem;
    }
    .social a{
        color: var(--clr-Black);
        font-size: 2rem;
        margin-left: 1rem;
    }
    @media screen and (min-width: 1024px){
        .about_section h1{
            font-size: 8rem;
        }
        .about_section p{
            font-size: 2rem;
        }
        .me .me_img{
            flex-direction: row;
            justify-content: center;
            align-items: center;
        }
        .me h1{
            font-size: 8rem;
        }
        .me .me_img p{
            font-size: 2rem;
        text-align: justify;
        }
        .social{
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
        }
    }
</style>
