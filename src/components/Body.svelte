<script>
    import Logo from '../img/logo.png'
    import Castle  from '../img/castelo.png'
    import NavButton from './NavButton.svelte';
     

    export let togglePage;
    export let pageStatus;
</script>

<img class="background" src={Castle} alt="">
<section>
    
    <div class="container">

         <div class="container-content">
             <p>
                 design, conteúdo & filtros para <span class="italic">agências</span> e marcas incríveis.
             </p>
             <p>
                 a sua super personalidade com a <span class="bold">força do</span> 🐐 para <span class="italic">uma marca autêntica e destacada no mundo.</span>
             </p>        
         </div>

         <div class="container-logo">
            <h1>
                 <img src={Logo} alt="website logo">
            </h1>
         </div>
        
    </div>

    <NavButton togglePage={togglePage} pageStatus={pageStatus}/>
</section>

<style>

    section {
        width: 100%;
        height: 100vh;
        display: flex;
        justify-content: center;
        flex-direction: column;
        align-items: center;
        gap: 10rem;
    }

    .container {
        display: flex;
        align-items: center;
        gap: 6rem;
        margin: 0 2rem;
    }

    .background {
        position:fixed;
        width: 100%;
        height: 100%;
        z-index: 0;
        object-fit: cover;
    }

    .container-logo > h1 > img {
        max-width: 400px;
        min-width: 350px;
        width: 100%;
    }

    .container-content {
        max-width: 550px;
        min-width: 300px;
        width: 100%;
        height: 110px;
        display: flex;
        flex-flow: column;
        justify-content: space-between;
        align-items: center;
        gap: 2rem;
    }

    .container-content > p {
        font-size: 1.2rem;
        text-transform: uppercase;
        color: #DE8D78;
        line-height: 1.3rem;
    }

    .container-content > p >.italic {
        font-weight: 300;
        font-style: italic;   
    }

    .container-content > p > .bold {
        font-weight: 600;
    }

    @media screen and (max-width: 768px) {
        section {
            flex-flow: column;
            justify-content: space-evenly;
            align-items: center;
            gap: 1rem;
        }
         .container {
            flex-flow: column-reverse;
            justify-content: space-evenly;
            align-items: center;
            gap: 1rem;
        }
        .container-logo > h1 > img {
            max-width: 350px;
            min-width: 150px;
            margin-left: 10px;
        }

        .container-content {
            max-width: 400px;
            font-size: 0.9rem;
        }
    }
</style>

