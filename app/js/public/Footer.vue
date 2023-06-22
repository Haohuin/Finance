<template>
  <panel :class="$style.panel" title="公司信息">
    <ul :class="$style.content">
      <li>
        <img src="//img" alt="">
      </li>
    </ul>
  </panel>
</template>

<script>

import panel from "../core/Panel.vue"
export default {
  name: "Footer",
  components: { panel },
}
</script>

<style lang="scss" module>
@import "../../css/element.scss";
.panel{
  @include panel;

}
</style>
