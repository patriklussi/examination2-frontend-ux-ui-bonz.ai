<template>
  <div class="wrapper">
    <section class="bookingCardWrap">
      <article class="bookingCard">
        <div class="contentBox">
          <article class="left">
            <img src="../assets/photos/06-day.jpg" alt="" />
          </article>
          <article class="right">
            <h2>Type 3</h2>
            <p>
              Lorem Ipsum is simply <br />
              dummy text of the <br />
              printing and typesetting <br />
              industry.
            </p>
          </article>
        </div>
        <article class="addOnBox">
          <div class="AddOnWrap">
            <p>
              On-demand drone-delivered coffee <br />
              100 SEK
            </p>
            <input class="blackCheckBox" type="radio" name="" id="" />
          </div>
          <div class="AddOnWrap">
            <p>
              On-demand drone delivered food <br />
              200 SEK
            </p>
            <input class="blackCheckBox" type="radio" name="" id="" />
          </div>
          <p class="total">Total 1100sek</p>
          <button class="button">Book</button>
        </article>
      </article>
    </section>

    <section class="mobileBookingCard">
      <h2 class="mobileTitleH2">Type 3</h2>
      <img src="../assets/photos/06-day.jpg" alt="" />
      <p class="mobilePVersionOne">
        Lorem Ipsum is simply dummy text of the <br />
        printing and typesetting industry.
      </p>
      <div class="checkBoxWrap">
        <p class="mobilePVersionOne">
          On-demand drone-delivered coffee <br />
          100 SEK
        </p>
        <input class="blackCheckBox" type="radio" name="" id="" />
      </div>

      <div class="checkBoxWrap">
        <p class="mobilePVersionOne">
          On-demand drone delivered food <br />
          200 SEK
        </p>
        <input class="blackCheckBox" type="radio" name="" id="" />
      </div>
      <p class="mobilePVersionOne">Total 1100 SEK</p>
      <button class="mobileButton">Book now</button>
    </section>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
</style>
