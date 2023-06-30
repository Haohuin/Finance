<template>
  <div :class="$style.background">
    <my-home-header/>
    <my-home-slider/>
    <my-home-interest/>
  </div>
</template>

<script>
import MyHomeHeader from "./MyHomeHeader.vue"
import MyHomeSlider from "./MyHomeSlider.vue"
import MyHomeInterest from "./MyHomeInterest.vue"
export default {
  name: "Index",
  components: { MyHomeInterest, MyHomeSlider, MyHomeHeader },
}
</script>

<style lang="scss" module>
.background{
  background-color: white;
}
</style>
