<script>
  import Header from './components/Header.svelte'
  import Body from './components/Body.svelte'
  import ContactPage from './components/ContactPage.svelte';
  import { slide } from 'svelte/transition';

  let pageStatus = false;

  const togglePage = () => {
        pageStatus ? pageStatus = false : pageStatus = true;
    }

</script>

{#if !pageStatus}
  <div class="main" in:slide out:slide>
      <Header/>
      <div class="body">
        <Body togglePage={togglePage} pageStatus={pageStatus}/>
      </div>
  </div>
{/if}

{#if pageStatus}
  <div class="main" in:slide out:slide>
      <div class="body">
        <ContactPage togglePage={togglePage} pageStatus={pageStatus}/>
      </div>
  </div>
{/if}

<style>
  .main {
    /* background-color: red; */
    width: 100vw;
    height: 100vh;
    width: 100%;
  }

  .body {
    width: 100vw ;
    height: 100vh ;
    display: flex;
    align-items: center;
    justify-content: center;
  }
</style>