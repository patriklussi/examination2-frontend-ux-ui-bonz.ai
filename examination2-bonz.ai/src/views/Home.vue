<template>
  <div class="home">
    <Nav/>
    <header class="pageHeader"></header>
    <main class="mainSection"></main>
    <footer class="pageFooter"></footer>
   
  </div>
</template>

<script>
// @ is an alias to /src
import Nav from "../components/Nav.vue";

export default {
  name: 'Home',
  components: {
  Nav
  }
}
</script>

<style lang="scss" scoped>



</style>
