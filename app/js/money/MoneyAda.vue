<template>
  <Panel :class="$style.panel" title="神券享">
    <section :class="$style.content">
      <img src="//img12.360buyimg.com/jrpmobile/jfs/t5842/235/8356236245/38364/2112fd7e/597a95d4Ne01da140.png?width=750&height=270" alt="">
    </section>
  </Panel>
</template>

<script>

import Panel from "../core/Panel.vue"
export default {
  name: "MoneyAda",
  components: { Panel },
}
</script>

<style lang="scss" module>
@import "../../css/element.scss";
.panel{
  @include panel;
  /*消除标题*/
  >h4{
    display: none;
  }
  .content{
    img{
      width: 100%;
      height: 230px;
      display: block;
    }
  }
}
</style>
