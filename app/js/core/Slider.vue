<template>
  <section :class="cname">
    <swiper :options="options" :not-next-tick="options.notNextTick">
      <swiper-slide v-for="item in items" :key="item.href">
        <router-link to="{ name: item.href }">
          <img :src="item.src" alt="">
        </router-link>
      </swiper-slide>
      <div v-if="options.pagination" slot="pagination" class="swiper-pagination"/>
    </swiper>
  </section>
</template>

<script>
/* 在awesome-swiper3.x 中，只能use low captial */
import { swiper, swiperSlider } from "vue-awesome-swiper"

export default {
  name: "Slider",
  components: {
    swiper,
    swiperSlider,
  },
  props: {
    cname: {
      type: String,
      default: "",
    },
    items: {
      type: Array,
      default() {
        return []
      },
    },
    options: {
      type: Object,
      default() {
        return {
          autoplay: true,
          loop: true,
          pagination: {
            el: ".swiper-pagination",
          },
          notNextTick: false,
        }
      },
    },
  },
}
</script>

<style lang="css">
@import "~swiper/dist/css/swiper.css";
</style>
