<script>
    import FaAngleDown from 'svelte-icons/fa/FaAngleDown.svelte'
    import FaAngleUp from 'svelte-icons/fa/FaAngleUp.svelte'
    export let togglePage;
    export let pageStatus;
</script>

{#if !pageStatus}
<button on:click={togglePage}>
   <FaAngleDown/> 
</button>
{/if}

{#if pageStatus}
<button on:click={togglePage}>
   <FaAngleUp/> 
</button>
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
