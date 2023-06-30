<template>
  <Panel :class="$style.panel">
    <section :class="$style.content">
      <dl v-for="item in items" :class="$style.item" :key="item.title">
        <dt>{{ item.title }}<span>{{ item.sub }}</span></dt>
        <dt>{{ item.rate }}</dt>
        <dt>{{ item.text }}</dt>
      </dl>
    </section>
  </Panel>
</template>

<script>
import Panel from "../core/Panel.vue"
export default {
  name: "Money",
  components: { Panel },
  data() {
    return {
      items: [{
        title: "定期理财",
        sub: "理财首选",
        rate: "5.60%",
        text: "历史年化回报率",
      }, {
        title: "小白理财",
        sub: "理财首选",
        rate: "4.22%",
        text: "7日年化收益率",
      }, {
        title: "月月盈",
        sub: "养老保障",
        rate: "5%",
        text: "七日年化收益率",
      }, {
        title: "小白基金",
        sub: "天天赚钱",
        rate: "4.27%",
        text: "7日年化收益率",
      }],
    }
  },
}
</script>

<style lang="scss" module>
@import "../../css/element.scss";
.panel{
  @include panel;
  .content{
    @include flex(row);
    justify-content: space-around;
    box-sizing: border-box;
  }
}
</style>
