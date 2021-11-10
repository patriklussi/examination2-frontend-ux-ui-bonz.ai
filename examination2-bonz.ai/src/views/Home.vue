<template>
  <div class="home">
    <nav class="navigation">
    <h1>Bonz.Ai</h1> 
    <div class="navWrap">
    <h2>Stay</h2>
    <h2>About</h2>
    <button class="generalButton">Book</button>
    </div>
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
  justify-content: space-between;
  h2 {
    font-weight: 700;
  }
  h2:hover {
    cursor: pointer;
  }
 
  .navWrap {
    @include center;
    width: 402px;
    justify-content: space-between;
    margin-right: 92px;
  }
 h1 {
   margin-left: 89px;
 }
  .rectangle {
  width:100%;
  height: 11px;
  background: #08F7FE;
  position: absolute;
  top:121px;


} 
}

</style>
