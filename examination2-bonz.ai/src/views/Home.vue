<template>
  <div class="home">
    <nav class="navigation"><h1>Bonz.Ai</h1> <article class="rectangle"></article></nav>
    <header class="pageHeader"></header>
    <main class="mainSection"></main>
    <footer class="pageFooter"></footer>
   
  </div>
</template>

<script>
// @ is an alias to /src


export default {
  name: 'Home',
  components: {
  
  }
}
</script>

<style lang="scss" scoped>
@import '../scss/_mixins.scss';
.navigation {
  width: 100%;
 
  height: 132px;
  background: #00C2BA;
  @include center;
  flex-direction: column;
  justify-content: flex-end;
 
  .rectangle {
  width:100%;
  height: 11px;
  background: #08F7FE;
  h1 {
    align-self: center;
    justify-self: center;
  }

  } 
}

</style>
