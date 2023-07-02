<script>
    import CityPicture from '../img/city.png'
    import Text from '../img/text2.png'
    import NavButton from './NavButton.svelte';
    import LinkButton from './LinkButton.svelte';

    export let togglePage;
    export let pageStatus

    const contacts = [{
        id: 'whatsapp',
        text: 'WHATSAPP PARA ORÇAMENTOS!',
        link: 'https://wa.me/556299127500'
    },{
        id: 'behance',
        text: 'PORTFÓLIO NO BEHANCE',
        link: 'https://www.behance.net/estudiocapra'
    },{
        id: 'instagram',
        text: 'INSTAGRAM',
        link: 'https://www.instagram.com/estudio.capra/'
    }]

</script>

<img class="background" src={CityPicture} alt="background">
<section class="container-section">
    <NavButton togglePage={togglePage} pageStatus={pageStatus}/>

    <div class="container">
        <img src={Text} alt="Call me beep me">

        <div>
            {#each contacts as { id, text, link}}
                <LinkButton id={id} text={text} link={link}/>
            {/each}
        </div>
    </div>

</section>

<style>

    .container-section {
        width: 100vw;
        height: 100vh;
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 4rem;
        background-color: #FE99A9;
    }
    
    .background {
        position:fixed;
        width: 100%;
        height: 100%;
        z-index: 0;
        object-fit: cover;
    }
    
    .container {
        width: 100vw;
        z-index: 2;
        text-align: center;
        display: flex;
        flex-flow: column;
        align-items: center;
    }

    .container > div {
        display: flex;
        flex-flow: column;
        gap: 0.5rem;
    }

    .container > img {
        max-width: 400px;
        min-width: 200px;
        width: 100%;
    }
    
    @media screen and (max-width: 768px) {
    
        .container > img {
        max-width: 300px;
        min-width: 200px;
        width: 100%;
    }
}
</style>