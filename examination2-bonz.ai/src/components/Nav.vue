<template>
  <div class="nav-wrapper">
    <Overlay class="overlay" v-on:turnOff="toggleHamburgerOverlayOff" v-if="toggleHamburger" />
      <nav class="navigation">
     <div class="titleWrap">
        <img class="logoBonz" src="../assets/logo/bonz.ai-logo-black_symbol.svg" alt="">
       <h1 class="navHone" @click="goToMainPage">Bonz.Ai</h1>

     </div>
  
    <img @click="toggleHamburgerOverlay" class="hamburgerButton" src="../assets/icons/hamburger.svg" alt="">
    <div class="navWrap">
    <h2 >Stay</h2>
    <h2 >About</h2>
    <button @click="toggleToPage" class="button">Book</button>
    </div>
       
    </nav>
  </div>
</template>

<script>
import Overlay from "../components/hamburgerMenu.vue";
export default {
  components: {
    Overlay,
  },
  data:()=>{
  return {
    toggleHamburger:false,
  }
  },
methods:{
  toggleToPage(){
    this.$router.push("/about");
  },
  goToMainPage(){
   this.$router.push("/");
  },
  toggleHamburgerOverlay(){
   this.toggleHamburger = true;
  },
  toggleHamburgerOverlayOff(){
     this.toggleHamburger = false;
  }
}
}
</script>

<style  lang="scss" scoped>
@import '../scss/_mixins.scss';
@import '../scss/_components.scss';
.navHone:hover {cursor: pointer;}
.titleWrap {
  widows: 172px;
  display: flex;
  margin-left: 89px;
  h1 {
    margin-top: 5px;
  }
.logoBonz {
      height: 45px;  
}

}

  

@media screen and (max-width:500px) {
  .overlay {
    position: absolute;
  }
 .navigation {
   .navWrap {
     display:none;
   }
   .titleWrap {
     margin-left:18px;
     h1 {
     margin:0;
     margin-top: 12px;
     font-size: 1rem;

   
   }

   }
    
   
   .rectangle {
     display:none;
   }
   height: 60px;
   .hamburgerButton {
   display: block;
   margin-right: 18px;
   
 }
 .hamburgerButton:hover {
   cursor: pointer;
 }
 }
 
}
</style>