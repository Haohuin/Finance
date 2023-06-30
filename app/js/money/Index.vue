<template>
  <div>
    <Header/>
    <money-slider/>
    <money-ada/>
    <money/>
    <money-adb/>
    <money-finance/>
    <money-adc/>
    <Footer/>
    <Navbar/>
  </div>
</template>

<script>
import Header from "../public/Header.vue"
import Footer from "../public/Footer.vue"
import Navbar from "../public/Navbar.vue"
import MoneySlider from "./MoneySlider.vue"
import MoneyFinance from "./MoneyFinance.vue"
import Money from "./Money.vue"
import MoneyAdb from "./MoneyAdb.vue"
import MoneyAdc from "./MoneyAdc.vue"
import MoneyAda from "./MoneyAda.vue"

export default {
  name: "Index",
  components: { MoneyAda, MoneyAdb, MoneyAdc, MoneyFinance, MoneySlider, Money, Navbar, Footer, Header },
}
</script>

<style scoped>

</style>
