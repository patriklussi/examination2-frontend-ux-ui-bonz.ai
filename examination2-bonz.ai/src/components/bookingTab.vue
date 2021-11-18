<template>
  <div class="wrapperBookingTab">
    <section class="bookingTab">
      <article class="bookingTabArticle">
        <div class="textBox">
          <p>Check in</p>
          <br />
          <p class="pTwo">Dec 22</p>
        </div>
        <img src="../assets/icons/calendar.svg" alt="icon" />
        <div class="bookingTabLine"></div>
      </article>
      <article class="bookingTabArticle">
        <div class="textBox">
          <p>Check in</p>
          <br />
          <p class="pTwo">Dec 22</p>
        </div>
        <img src="../assets/icons/calendar.svg" alt="icon" />
        <div class="bookingTabLine"></div>
      </article>
      <article class="bookingTabArticle">
        <div class="textBox">
          <p>Guests</p>
          <br />
          <p>1 guest</p>
        </div>
        <img src="../assets/icons/guest.svg" alt="icon" />
        <div class="bookingTabLine"></div>
      </article>
      <article class="bookingTabArticle">
        <div class="textBox">
          <p>Check in</p>
          <br />
          <p>Dec 22</p>
        </div>
        <img src="../assets/icons/thiccHouse.svg" alt="icon" />
      </article>
    </section>

    <section class="mobileBookingTab">
      <article class="bookingTabArticle">
        <div class="textBox">
          <p class="bigP">Check in</p>

          <p class="pTwo">Dec 22</p>
        </div>
        <img src="../assets/icons/calendar.svg" alt="icon" />
      </article>
      <div class="bookingTabLine"></div>
      <article class="bookingTabArticle">
        <div class="textBox">
          <p class="bigP">Check out</p>

          <p class="pTwo">Dec 26</p>
        </div>
        <img src="../assets/icons/calendar.svg" alt="icon" />
      </article>
    </section>

    <section class="mobileBookingTab">
      <article class="bookingTabArticle">
        <div class="textBox">
          <p class="bigP">Guests</p>

          <p class="pTwo">1 guest</p>
        </div>
        <img src="../assets/icons/guest.svg" alt="icon" />
      </article>
      <div class="bookingTabLine"></div>
      <article class="bookingTabArticle">
        <div class="textBoxTwo">
          <p class="bigP">No of rooms</p>

          <p class="pTwo">1 room</p>
        </div>
        <img src="../assets/icons/calendar.svg" alt="icon" />
      </article>
    </section>
  </div>
</template>

<script>
export default {
  components: {},
  data: function () {
    return {
      toggle: true,
    };
  },
  methods: {
    test() {
      this.toggle = false;
      console.log("hello");
    },
  },
};
</script>

<style lang="scss" scoped>
@media screen and (max-width: 500px) {
  .mobileBookingTab {
    margin-bottom: 18px;
  }
}
</style>
