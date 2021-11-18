<template>
  <section class="paymentDetailsWrap">
    <h1 class="h1Title">Costumer info</h1>
    <article class="pdBox">
        
            <label height="73px" for="name">Name*</label>
            <input id="name" placeholder="Enter name" type="text">
            <label for="email">Email*</label>
            <input id="email" placeholder="Enter email" type="text">
            <label for="phone">Phone number</label>
            <input id="email" placeholder="Enter phone number" type="text">
       
    </article>
    <article class="rButtonBox">
        <p class="pDetailsp">Please confirm that the costumer is atleast 18 years old!</p>
        <input class="blackCheckBox" type="radio">
    </article>
    <button  @click="emitToParent" class="bookingButton">Continue</button>
    <button  @click="emitToParent" class="mobileButton">Continue</button>
</section>
</template>

<script>
export default {
methods:{
  emitToParent(){
    this.$emit("yoyo");
  }
}
}
</script>

<style lang="scss" scoped>

</style>