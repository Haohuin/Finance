<template lang="html">
  <div>
    <Header/>
    <home-slider/>
    <home-novice/>
    <home-borrow/>
    <home-money/>
    <home-product/>
    <home-life/>
    <Footer/>
  </div>
</template>
<script>
import Header from "../public/Header.vue"
import Footer from "../public/Footer.vue"
import HomeSlider from "./HomeSlider.vue"
import HomeNovice from "./HomeNovice.vue"
import HomeBorrow from "./HomeBorrow.vue"
import HomeMoney from "./HomeMoney.vue"
import HomeProduct from "./HomeProduct.vue"
import HomeLife from "./HomeLife.vue"
export default {
  components: { Footer, HomeLife, HomeProduct, HomeMoney, HomeBorrow, HomeNovice, HomeSlider, Header },
}
</script>

<style lang="scss" module>
</style>
