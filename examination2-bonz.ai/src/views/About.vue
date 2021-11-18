<template>
  <div class="wrapper">
    <Nav />
    <div v-if="toggleWrap" class="Stormcloak">
      <div class="item-wrapper">
        <h1>Booking</h1>
        <bookingTab class="test" />
        <BookingCardOne v-on:addToCompleted="addToCompleted" class="testTwo" />
        <BookingCardTwo class="testTwo" />
        <BookingCardThree class="testTwo" />
        <BookingCardFour class="testTwo" />
        <h1 v-if="!toggleCompleted">Book a room!</h1>
        <CompletedBookingCard
          v-if="toggleCompleted"
          class="testThree"
          v-on:goToPayment="toggleFunc"
        />
      </div>
    </div>
    <PaymentDetails v-on:yoyo="toggleToNext" class="pmDetails" v-if="toggler" />
    <CreditCardDetails class="ccDetails" v-if="toggle" />
    <Footer />
  </div>
</template>

<script>
import Nav from "../components/Nav.vue";
import Footer from "../components/Foot.vue";
import bookingTab from "../components/bookingTab.vue";
import BookingCardOne from "../components/BookingCardOne.vue";
import BookingCardTwo from "../components/BookingCardTwo.vue";
import BookingCardThree from "../components/BookingCardThree.vue";
import BookingCardFour from "../components/BookingCardFour.vue";
import CompletedBookingCard from "../components/CompletedBookingCard.vue";
import CreditCardDetails from "../components/creditCardDetails.vue";
import PaymentDetails from "../components/paymentDetails.vue";
export default {
  components: {
    Nav,
    Footer,
    bookingTab,
    BookingCardOne,
    BookingCardTwo,
    BookingCardThree,
    BookingCardFour,
    CompletedBookingCard,
    CreditCardDetails,
    PaymentDetails,
  },
  data: function () {
    return {
      toggle: false,

      toggleCompleted: false,
      toggler: false,
      toggleWrap: true,
    };
  },
  methods: {
    toggleFunc() {
      this.toggleCompleted = false;
      this.toggler = true;
      this.toggleWrap = false;
    },
    addToCompleted() {
      this.toggleCompleted = true;
    },
    toggleToNext() {
      this.toggle = true;
      this.toggler = false;
    },
  },
};
</script>

<style lang="scss" scoped>
@import "../scss/_mixins.scss";
.wrapper {
  .pmDetails {
    margin: auto;
    margin-bottom: 210px;
    margin-top: 124px;
  }
  .ccDetails {
    margin: auto;
    margin-top: 124px;
    margin-bottom: 319px;
  }
  h1 {
    text-align: center;
    font-weight: 500;
    font-size: 36px;
    line-height: 30px;
    margin-top: 47px;
    margin-bottom: 63px;
  }
  width: 100%;
  .Stormcloak {
    width: 100%;
    @include center;
    flex-direction: column;
    .item-wrapper {
      width: 75%;
      @include center;
      flex-direction: column;
      .test {
        margin-bottom: 3.5rem;
      }
      .testTwo {
        margin-bottom: 3.5rem;
      }
      .testThree {
        margin-bottom: 80px;
      }
    }
  }
}

@media screen and (max-width: 500px) {
  .Stormcloak {
    .item-wrapper {
      width: 90%;
    }
  }
}
</style>


