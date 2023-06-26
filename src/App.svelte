<script>
  import Header from './components/Header.svelte'
  import Body from './components/Body.svelte'
</script>

<div class="main">
    <Header/>
    <div class="body">
      <Body/>
    </div>
</div>

<style>
  .main {
    /* background-color: red; */
    width: 100vw;
    height: 100vh;
    width: 100%;
    background-image: url('./img/castelo.png');
  }

  .body {
    width: 100vw ;
    height: 100vh ;
    display: flex;
    align-items: center;
    justify-content: center;
  }
</style>