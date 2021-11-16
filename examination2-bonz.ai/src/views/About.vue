<template>
  <div class="wrapper">
   <Nav/>
    <div class="grid-wrapper">
      <h1>Booking</h1>
      <bookingTab/>
      <BookingCard/>
      <BookingCard/>
      <BookingCard/>
      <BookingCard/>
      <CompletedBookingCard/>
    </div>

   <Footer/>
  </div>
</template>

<script>
import Nav from "../components/Nav.vue"
import Footer from "../components/Foot.vue";
import bookingTab from "../components/bookingTab.vue";
import BookingCard from "../components/BookingCard.vue";
import CompletedBookingCard from "../components/CompletedBookingCard.vue";
export default {
components: {
  Nav,
  Footer,
  bookingTab,
  BookingCard,
  CompletedBookingCard
}
}
</script>

<style lang="scss" scoped>

.wrapper {

}
  .grid-wrapper {
    display:grid;
    max-width: 1205px;
    grid-template-columns: auto;
    margin: auto;
    row-gap: 2rem;
    
  }
</style>


