<script>
    import BoopAction from "./BoopAction.svelte";

    export let id;
    export let text;
    export let link;


</script>

<BoopAction boopParams={{y: 3, timing: 200}}>
    <a href={link} target="_blank">
        <button>
            {text}
        </button>
    </a>
</BoopAction>

<style>
    a {
        text-decoration: none;
        font-weight: bold;
    }

    button{
        color: #F7D9CF;
        background-color: transparent;
        border: 0.2rem solid #EE766F;
        border-radius: 0.3rem;
        font-weight: bold;
        font-size: 1.1rem;
        min-width: 270px;
        max-width: 350px;
        width: 100%;
        padding: 2px 10px; 
    }

    @media screen and (min-width: 768px) {
    
        button {
            font-size: 1.6rem;
            border: 0.3rem solid #EE766F;
            max-width: 400px;
        }
    }
</style>