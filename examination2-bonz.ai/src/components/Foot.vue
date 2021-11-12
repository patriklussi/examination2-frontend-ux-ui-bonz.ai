<template>
  <div class="foot-wrapper">
        <article class="iconBox">
        <img src="../assets/icons/facebook.svg" alt="">
        <img src="../assets/icons/twitter.svg" alt="">
        <img src="../assets/icons/instagram.svg" alt="">
        </article>
        <p>© Copyright 2021 Bonz.AI</p>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
@import "../scss/_mixins.scss";
@import "../scss/_components.scss";
    .foot-wrapper {
        width: 100%;
        height: 376px;
        background: #2B2319;
        @include center;
        flex-direction: column;
        .iconBox {
          
         width: 255px;
          display: flex;
          justify-content: space-between;
          img {
          
          }
        }
        p {
          font-size: 22px;
          color:white;
          margin-top:34px;
        }
    }

    @media screen and (max-width:500px) { 

      .foot-wrapper {
        height: 208px;
         .iconBox {
        width:156px;
        img {
          height: 26px;
        }
        justify-content: space-evenly;
      }
      p {
        font-size: 12px;
        font-weight: 400;
        margin-top:17px;
      }
      }
     
    }
</style>