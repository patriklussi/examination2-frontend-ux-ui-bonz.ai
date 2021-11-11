<template>
  <div class="wrapper">
    <Nav />
    <header class="pageHeader">
      <article class="titleBox">
        <h1>Bonz.Ai</h1>
        <h2>An Ai-Powered Eco-Stay</h2>
      </article>
    </header>
    <main class="mainSection">
      <h2>Bonz.Ai</h2>
      <p>
        Hello from Bonz.AI 👋 we are thrilled to welcome you to our AI-powered
        eco-stay at Bohuslän to the north of Gothenburg, Sweden.
        <br>
        <br>
         We believe in
        offering a personalized stay like none other, by bringing the ultimate
        contact-less experience to you at your finger tips - on your mobile
        device. Sit back, relax and let Bonz.AI take care of you.
      </p>
      <button class="generalButton">Book now</button>
    </main>
    <section class="roomView"><h1>Select Your Stay</h1>
      <article class="card">
        <article class="left"> <img class="cardImg" src="../assets/photos/01-night.jpg" alt=""></article>
        <article class="right">
         
        <h2>Type 1</h2>
        <p>Lorem Ipsum is simply dummy text of the  <br>  printing and typesetting <br> industry.</p>
      
      
        <button class="generalButton">Book</button>
          </article>
      </article>
    
    </section>
    <Foot />
  </div>
</template>

<script>
// @ is an alias to /src
import Nav from "../components/Nav.vue";
import Foot from "../components/Foot.vue";

export default {
  name: "Home",
  components: {
    Nav,
    Foot
  },
}
</script>

<style lang="scss" scoped>
@import "../scss/_mixins.scss";
@import "../scss/_components.scss";
.wrapper {
  @include grid-column-auto;
}
.pageHeader {
  height: 810px;
  //  @include center;
  // flex-direction: column;

  .titleBox {
    border-bottom: 6px solid #08f7fe;
    width: 642px;
    display: flex;
    flex-direction: column;
    margin-left: 167px;
    margin-top: 91px;
    h1 {
      font-size: 4rem;
      color: #00c2ba;
      align-self: center;
      margin-bottom: 50px;
    }
    h2 {
      font-size: 3rem;
      font-weight: lighter;
      color: white;
      align-self: center;
      margin-bottom: 39px;
    }
  }
  background: url("../assets/photos/02-night.jpg");
  background-repeat: no-repeat, repeat;
  background-size: cover;
  background-position: center;
}
.mainSection {
  height: 646px;
  background: #d3cfc347;
 @include center;
 flex-direction: column;
 p {
   width:60%;
   font-size: 2rem;
   margin:0;
 }
 h2 {
   font-size: 2.25rem;
  
 }
 .generalButton {
 
 }
}
.roomView {
  height: 859px;
  .card {
    
    display: flex;
    .left {
      flex-basis: 50%;
    display: flex;
    }
    .right {
  flex-basis: 50%;
  @include space-between;
  
  flex-direction: column;
      p {
        font-size: 20px;
        font-weight: 600;
      }
  }
   width: max-content;
  .cardImg {
   height: 250px;
   width: 100%;
}
}
}



</style>
