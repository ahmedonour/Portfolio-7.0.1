<script>
	import { fly } from 'svelte/transition';
</script>

<svelte:head>
	<title>Ahmed Suliman | Contact Us</title>
</svelte:head>
<main
	in:fly={{ y: 200, duration: 500, delay: 500 }}
	out:fly={{ y: -200, duration: 500, delay: 300 }}
>
	<div class="contactus-text">
		<img src="CONTACT US.svg" alt="contact-us" />
		<h1>Have a project ! Let’s discuss</h1>
		<p>
			Thank you for getting in touch! Kindly.<br />
			Fill the form, have a great day!
		</p>
	</div>
	<form action="https://formsubmit.co/ahmedonour.49@gmail.com" method="POST">
		<div class="inputs">
			<input type="text" name="name" placeholder="Your Name" />
			<input type="text" name="email" placeholder="Your Email" />
		</div>
		<div class="inputs">
			<input type="text" name="number" placeholder="Phone Number" />
			<input type="text" name="country" placeholder="Country" />
		</div>
		<textarea name="message" cols="30" rows="4" placeholder="Message" />
        <button type="submit">Submit</button>
	</form>
</main>

<style>
    main{
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        width: 100vw;
    }
    main .contactus-text{
        width: 100%;
        height: 50%;
        display: grid;
        place-items: center;
    }
    main .contactus-text img{
        position: relative;
        top: 20px;
        left: -20px;
        width: 90%;
    }
    main .contactus-text h1{
        color: var(--clr-Black);

        font-family: var(--ff-main);
        text-align: center;
        font-size: 2.5rem;
    }
    main .contactus-text p{
        color: var(--clr-Black);

        font-family: var(--ff-p);
        text-align: center;
        font-weight: 500;
    }
    form{
        display: grid;
        place-items: center;
        width: 75vw;
        margin-top: 1rem;
    }
    form .inputs{
        width: fit-content;

    }
    form .inputs input{
        width: 100%;
        background-color: transparent;
        border: none;
        outline: none;
        padding: 1rem;
        color: var(--clr-Black);
        font-family: var(--ff-p);
        font-size: 1rem;
        font-weight: 500;
        border-bottom: 1px solid var(--clr-Black);
    }
    /* form .inputs input::placeholder{
        font-family: var(--ff-p);
        font-weight: 600;
        color: var(--clr-Black);
    } */
	form textarea {
        padding: 1rem;
        width: 100%;
        background-color: transparent;

        border: none;
        outline: none;
		resize: none;
        border-bottom: 1px solid var(--clr-Black);

	}
    form button{
        width: 100%;
        padding: 1rem;
        background-color: var(--clr-yellow);
        border: none;
        font-family: var(--ff-p);
        font-weight: 600;
        font-size: 1rem;
        margin-top: 1rem;
        color: var(--clr-Black);
    }
    ::placeholder{
        font-family: var(--ff-p);
        font-weight: 600;
        color: var(--clr-Black);
        
    }
    @media screen and (min-width: 1024px){
        main{
            flex-direction: row;
        }
        main .contactus-text{
            width: 50vw;
            display: flex;
            flex-direction: column;
            justify-content: flex-start;
            align-items: flex-start;
            padding: 0rem 0 0 10rem;
        }
        main .contactus-text img{
        position: absolute;
        top: 160px;
        left: -10px;
        width: 60%;
        z-index: -1;
    }
    main .contactus-text h1{
        text-align: left;
        font-size: 4rem;
    }
    main .contactus-text p{
        text-align: left;
        font-weight: 500;
    }
        main form{
            width: 50vw;
            height: 60vh;
        margin-top: 1rem;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        }
        main form .inputs{
            display: flex;
            flex-direction: row;
            gap: 1rem;
        }
        main form textarea{
            width: 66%;
        }
        main form button{
            width: 66%;
            padding: .5rem;
            font-size: .8rem;
            transition: all .5s ease-in-out;
        }
        main form button:hover{
            cursor: pointer;
            background-color: var(--clr-Black);
            color: var(--clr-yellow);
        }
    }
</style>
