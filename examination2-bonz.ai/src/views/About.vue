<template>
  <div class="wrapper">
   <Nav/>
    <div class="grid-wrapper">
      <h1>Booking</h1>
      <bookingTab/>
      <BookingCardOne/>
      <BookingCardTwo/>
      <BookingCardThree/>
      <BookingCardFour/>
      <CompletedBookingCard/>
    </div>

   <Footer/>
  </div>
</template>

<script>
import Nav from "../components/Nav.vue"
import Footer from "../components/Foot.vue";
import bookingTab from "../components/bookingTab.vue";
import BookingCardOne from "../components/BookingCardOne.vue";
import BookingCardTwo from "../components/BookingCardTwo.vue";
import BookingCardThree from "../components/BookingCardThree.vue";
import BookingCardFour from "../components/BookingCardFour.vue";
import CompletedBookingCard from "../components/CompletedBookingCard.vue";
export default {
components: {
  Nav,
  Footer,
  bookingTab,
  BookingCardOne,
  BookingCardTwo,
  BookingCardThree,
  BookingCardFour,
  CompletedBookingCard
}
}
</script>

<style lang="scss" scoped>

    .wrapper {
      h1 {
        text-align: center;
        font-weight: 500;
        font-size: 36px;
        line-height: 30px;
        margin-top: 47px;
        margin-bottom: 63px;
      }
      width: 100%;
    }
  .grid-wrapper {
    display:grid;
    max-width: 1205px;
    grid-template-columns: auto;
    margin: auto;
    row-gap: 2rem;
    margin-bottom: 80px;
  }

  @media screen and (max-width:500px) { 

    .grid-wrapper {
      width: 100%;
    }
  }
</style>


