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
        <br />
        <br />
        We believe in offering a personalized stay like none other, by bringing
        the ultimate contact-less experience to you at your finger tips - on
        your mobile device. Sit back, relax and let Bonz.AI take care of you.
      </p>
      <button class="button">Book now</button>
    </main>
    <section class="roomView">
      <h1>Select your stay</h1>
      <section class="grid-container">
        <article class="card">
          <article class="left">
            <img class="cardImg" src="../assets/photos/01-night.jpg" alt="" />
          </article>
          <article class="right">
            <h2>Type 1</h2>
            <p>
              Lorem Ipsum is simply <br />
              dummy text of the <br />
              printing and typesetting <br />
              industry.
            </p>

            <button class="button">Book</button>
          </article>
        </article>
        <div class="wrapperMobile">
          <img
            class="chevronBoyOne"
            @click="chevronRight"
            src="../assets/icons/chevronLeft.svg"
            alt=""
          />

          <article v-if="!toggle" class="MobileCard">
            <h2>Type 1</h2>
            <img class="cardImg" src="../assets/photos/06-night.jpg" alt="" />
            <p>
              Lorem Ipsum is simply <br />
              dummy text of the <br />
              printing and typesetting <br />
              industry.
            </p>
            <button class="mobileButton">Book</button>
          </article>
          <article v-if="toggle" class="MobileCard">
            <h2>Type 2</h2>
            <img class="cardImg" src="../assets/photos/02-night.jpg" alt="" />
            <p>
              Lorem Ipsum is simply <br />
              dummy text of the <br />
              printing and typesetting <br />
              industry.
            </p>
            <button class="mobileButton">Book</button>
          </article>

          <img
            @click="chevronToggle"
            class="chevronBoyTwo"
            src="../assets/icons/chevronRight.svg"
            alt=""
          />
        </div>

        <article class="card">
          <article class="left">
            <img class="cardImg" src="../assets/photos/01-night.jpg" alt="" />
          </article>
          <article class="right">
            <h2>Type 1</h2>
            <p>
              Lorem Ipsum is simply <br />
              dummy text of the <br />
              printing and typesetting <br />
              industry.
            </p>

            <button class="button">Book</button>
          </article>
        </article>

        <article class="card">
          <article class="left">
            <img class="cardImg" src="../assets/photos/03-night.jpg" alt="" />
          </article>
          <article class="right">
            <h2>Type 3</h2>
            <p>
              Lorem Ipsum is simply <br />
              dummy text of the <br />
              printing and typesetting <br />
              industry.
            </p>

            <button class="button">Book</button>
          </article>
        </article>
        <article class="card">
          <article class="left">
            <img class="cardImg" src="../assets/photos/04-night.jpg" alt="" />
          </article>
          <article class="right">
            <h2>Type 4</h2>
            <p>
              Lorem Ipsum is simply <br />
              dummy text of the <br />
              printing and typesetting <br />
              industry.
            </p>

            <button class="button">Book</button>
          </article>
        </article>
      </section>
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
    Foot,
  },
  data: function () {
    return {
      toggle: false,
      toggleTwo: false,
      toggleThree: false,
    };
  },
  methods: {
    chevronToggle() {
      this.toggle = true;
    },
    chevronRight() {
      this.toggle = false;
    },
  },
};
</script>

<style lang="scss" scoped>
@import "../scss/_mixins.scss";
@import "../scss/_components.scss";
.wrapper {
  @include grid-column-auto;
}
.wrapperMobile {
  display: none;
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
  justify-content: space-evenly;
  h2 {
    font-size: 2.25rem;
  }
  p {
    width: 75%;
  }
}
.roomView {
  h1 {
    margin-bottom: 51px;
    font-size: 2.25rem;
    font-weight: 500;
  }
  height: 859px;
  @include center;
  flex-direction: column;

  .grid-container {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    max-width: 1500px;
    row-gap: 51px;
  }
  .MobileCard {
    display: None;
  }
  .card {
    display: flex;
    .left {
      flex-basis: 50%;
      display: flex;
    }
    .right {
      margin-left: 22px;
      flex-basis: 50%;
      @include space-between;

      flex-direction: column;
      p {
        font-size: 20px;
        font-weight: 600;
      }
    }

    .cardImg {
      height: 250px;
      width: 100%;
    }
  }
}

@media screen and (max-width: 500px) {
  .wrapperMobile {
    display: block;
    display: flex;
  }
  .chevronBoyOne {
    margin-right: 24px;
  }
  .chevronBoyTwo {
    margin-left: 24px;
  }

  .pageHeader {
    height: 290px;
    .titleBox {
      border-bottom: 1px solid #08f7fe;
      width: 249px;
      margin: 0;
      margin-top: 37px;
      margin-left: 4px;
      h1 {
        font-size: 30px;
        color: #00c2ba;
        align-self: center;
        margin: 0;
      }
      h2 {
        font-size: 20px;
        font-weight: 300;
        color: white;
        align-self: center;
        margin: 0;
      }
    }
  }

  .mainSection {
    p {
      font-size: 14px;
      font-weight: 600;
    }
    h2 {
      font-size: 24px;
    }
  }

  .roomView {
    .grid-container {
      grid-template-columns: repeat(1, 1fr);
      .card {
        display: none;
      }
      .MobileCard {
        h2 {
          width: 100%;
          height: 45.13px;
          background: #f2d4ae;
          @include center;
        }
        p {
          margin-bottom: 21px;
          margin-top: 7px;
        }
        @include center;
        flex-direction: column;
        width: 310px;
        box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
        img {
          margin-top: 39px;
          height: 191px;
          filter: drop-shadow(0px 4px 4px rgba(0, 0, 0, 0.25));
          width: 263px;
        }

        .generalButton {
          width: 100%;
          border-radius: 0;
        }
      }
    }
    h1 {
      font-size: 24px;
    }
  }
}
</style>
