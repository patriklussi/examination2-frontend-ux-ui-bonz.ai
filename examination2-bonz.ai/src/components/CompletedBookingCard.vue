<template>
  <div class="wrapper">
    <section class="completedBookingWrap">
      <h1>Your Booking</h1>
      <article class="middle">
        <article class="left">
          <p>Wed, Dec 22, 2021 - Sun, Dec 26, 2019</p>
          <p>1 Adult</p>
          <p>4 nights</p>
          <p>Room Type1</p>
          <p>Drone-delivered coffee included</p>
        </article>
        <article class="right">
          <img class="imgReplace" src="../assets/photos/03-day.jpg" alt="" />
          <p>Total 1100 SEK</p>
        </article>
      </article>

      <button @click="emitToAbout" class="bookingButton">
        Complete your booking
      </button>
    </section>

    <section class="mobileCard">
      <h1>Your booking</h1>
      <img class="imgReplace" src="../assets/photos/03-day.jpg" alt="" />
      <div class="textWrap">
        <p>Wed, Dec 22, 2021 - Sun, Dec 26, 2019</p>
        <p>1 Adult</p>
        <p>4 nights</p>
        <p>Room Type2</p>
        <p>Drone-delivered coffee included</p>

        <p>Total 1100 SEK</p>
      </div>
      <button @click="emitToAbout" class="mobileButton">
        Complete your booking
      </button>
    </section>
  </div>
</template>

<script>
export default {
  methods: {
    emitToAbout() {
      this.$emit("goToPayment");
    },
  },
};
</script>

<style lang="scss" scoped>
</style>