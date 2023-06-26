<script>
    import Logo from '../img/logo.png'
</script>

<section>
    <div>
        <p>
            design, conteúdo & filtros para <span class="italic">agências</span> e marcas incríveis.
        </p>
        <p>
            a sua super personalidade com a <span class="bold">força do</span> 🐐 para <span class="italic">uma marca autêntica e destacada no mundo.</span>
        </p>        
    </div>
    
   <h1>
        <img src={Logo} alt="website logo">
    </h1>
   
</section>

<style>
    section {
        display: flex;
        justify-content: center;
        align-items: center;
        gap: 4rem;
    }

    section > h1 > img {
        max-width: 400px;
        min-width: 150px;
        width: 100%;
    }

    section > div {
        max-width: 500px;
        max-width: 300px;
        width: 100%;
        height: 110px;
        display: flex;
        flex-flow: column;
        justify-content: space-between;
    }

    section > div > p {
        font-size: 0.9rem;
        text-transform: uppercase;
        color: #DE8D78;
        line-height: 1.2rem;
    }
    section > div > p >.italic {
        font-weight: 300;
        font-style: italic;   
    }
    section > div > p > .bold {
        font-weight: 600;
    }
</style>

