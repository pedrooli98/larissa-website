<script>
    import FaAngleDown from 'svelte-icons/fa/FaAngleDown.svelte'
    import FaAngleUp from 'svelte-icons/fa/FaAngleUp.svelte'
    import Boop from './Boop.svelte';
    import BoopAction from './BoopAction.svelte';
    export let togglePage;
    export let pageStatus;

    const handleAnimation = () => {

    }

</script>

{#if !pageStatus}
<BoopAction boopParams={{ scale: 1.2, timing: 200}}>
    <button on:click={togglePage}>
       <FaAngleDown/> 
    </button>
</BoopAction>

{/if}

{#if pageStatus}
<BoopAction boopParams={{ scale: 1.2, timing: 200}}>
    <button on:click={togglePage}>
       <FaAngleUp/> 
    </button>
</BoopAction>
{/if}

<style>

    button {
        z-index: 2;
    }

    button {
        background-color: transparent;
        border: none;
        color: #205394;
        max-width: 80px;
        min-width: 15px;
        width: 100%;
    }
</style>
