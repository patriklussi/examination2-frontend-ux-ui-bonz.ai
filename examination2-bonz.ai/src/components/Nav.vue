<template>
  <div class="nav-wrapper">
      <nav class="navigation">
    <h1>Bonz.Ai</h1> 
    <img class="hamburgerButton" src="../assets/icons/hamburger.svg" alt="">
    <div class="navWrap">
    <h2>Stay</h2>
    <h2>About</h2>
    <button class="generalButton">Book</button>
    </div>
       
    </nav>
  </div>
</template>

<script>
export default {

}
</script>

<style  lang="scss" scoped>
@import '../scss/_mixins.scss';
@import '../scss/_components.scss';


@media screen and (max-width:500px) {
 .navigation {
   .navWrap {
     display:none;
   }
 
   h1 {
     margin:0;
   }
   .rectangle {
     display:none;
   }
   height: 60px;
   .hamburgerButton {
   display: block;
   margin-right: 18px;
   
 }
 }
 
}
</style>