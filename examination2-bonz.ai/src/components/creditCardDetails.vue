<template>
  <section class="creditCardDetailsWrap">
    <h1 class="h1Title">Payment details</h1>
    <article class="cdBox">
      <label class="labelText" height="73px" for="name">Cardholder name</label>
      <input class="inputText" id="name" type="text" />
      <label class="labelText" for="email">Card Number</label>
      <input
        placeholder="XXXX-XXXX-XXXX"
        class="inputCardNumber"
        id="email"
        maxlength="16"
        type="number"
      />
    </article>
    <article class="inputBox">
      <div>
        <label class="smallLabel" for="date">Valid thru</label>
        <input placeholder="MM/YY" class="dateInput" id="date" type="text" />
      </div>
      <div>
        <label class="smallLabel" for="ccv">CCV/CVC</label>
        <input placeholder="xxx" class="ccvInput" id="ccv" type="text" />
      </div>
    </article>
    <button class="bookingButton">Book</button>
    <button class="mobileButton">Book</button>
  </section>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
@media screen and (max-width: 500px) {
}
</style>

