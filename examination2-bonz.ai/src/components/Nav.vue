<template>
  <div class="nav-wrapper">
      <nav class="navigation">
     <div class="titleWrap">
        <img class="logoBonz" src="../assets/logo/bonz.ai-logo-black_symbol.svg" alt="">
       <h1 @click="goToMainPage">Bonz.Ai</h1>

     </div>
  
    <img class="hamburgerButton" src="../assets/icons/hamburger.svg" alt="">
    <div class="navWrap">
    <h2 @click="toggleToPage">Stay</h2>
    <h2 >About</h2>
    <button class="generalButton">Book</button>
    </div>
       
    </nav>
  </div>
</template>

<script>
export default {
methods:{
  toggleToPage(){
    this.$router.push("/about");
  },
  goToMainPage(){
   this.$router.push("/");
  }
}
}
</script>

<style  lang="scss" scoped>
@import '../scss/_mixins.scss';
@import '../scss/_components.scss';
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
 }
 
}
</style>