<template>
  <div class="home">
    <nav class="navigation">
    <h1>Bonz.Ai</h1> 
 
    <h2>Stay</h2>
    <h2>About</h2>
    <button class="generalButton">Book</button>
  
       <article class="rectangle"></article>
    </nav>
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
@import '../scss/_components.scss';
.navigation {
  width: 100%;
 
  height: 132px;
  background: #00C2BA;
  @include center;
 
  
 
  .rectangle {
  width:100%;
  height: 11px;
  background: #08F7FE;
  position: absolute;
  top:121px;


} 
}

</style>
