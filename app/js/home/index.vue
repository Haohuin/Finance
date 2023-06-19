<template lang="html">
  <div>
    <Header/>
    <home-slider/>
    <home-novice/>
  </div>
</template>
<script>
import Header from "../public/Header.vue"
import HomeSlider from "./HomeSlider.vue"
import HomeNovice from "./HomeNovice.vue"
export default {
  components: { HomeNovice, HomeSlider, Header },
}
</script>

<style lang="scss" module>
</style>
