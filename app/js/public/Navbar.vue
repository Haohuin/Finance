<template>
  <panel :class="$style.panel" title="导航条">
    <ul :class="$style.content">
      <li>a</li>
    </ul>
  </panel>
</template>

<script>
import Panel from "../core/Panel.vue"
export default {
  name: "Navbar",
  components: { Panel },
}
</script>

<style lang="scss" module>
@import "../../css/element.scss";
.panel{
  @include panel;
  position: fixed;
  left: 0;
  right: 0;
  bottom: 0;
  height: 100px;
  .content{
    @include flex(row);
  }
}
</style>
