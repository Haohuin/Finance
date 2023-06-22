<template>
  <panel :class="$style.panel" title="理财精选">
    <section :class="$style.content">
      <dl v-for="item in items" :key="item.id" :class="$style.item">
        <dt>{{ item.title }} <span>{{ item.sub }}</span></dt>
        <dd>{{ item.rate }}</dd>
        <dd>{{ item.text }}</dd>
      </dl>
    </section>
  </panel>
</template>
<script>
import Panel from "../core/Panel.vue"
export default {
  name: "HomeMoney",
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
    /*利用伪元素实现区块之间的分隔线*/
    &:after{
      /*before和after伪元素必须使用content属性，该内容不可省略*/
      content: " ";
      display: block;
      width: 100%;
      height: 0;
      box-sizing: border-box;
      border-bottom: 1px solid #ddd;
      position: relative;
      top: -208px;
    }
    .item{
      position: relative;
      width: 50%;
      box-sizing: border-box;
      /*利用伪元素来实现分隔线*/
      &:after{
        position: absolute;
        content: " ";
        width: 1px;
        height: 136px;
        display: block;
        top: 50%;
        right: 0;
        margin-top: -68px;
        border-right: 1px solid #eee;
      }
      &:nth-child(2n){
        &:after{
          display: none;
        }
      }
      padding: 34px 16px;
      dt{
        font-size: 30px;
        line-height: 42px;
        color: #333;
        span{
          font-size: 22px;
          color: #ff5155;
          border: 1px solid #ff5155;
          padding: 0 8px;
          vertical-align: 1px;
          margin-left: 2px;
        }
      }
      dd {
        /*第二个百分比内容样式*/
        &:nth-child(2) {
          font-weight: 700;
          font-size: 44px;
          height: 58px;
          line-height: 58px;
          color: #ff5155;
          white-space: nowrap;
          text-overflow: ellipsis;
          overflow: hidden;
        }
        /*第三个文案内容样式，伪元素的高级用法*/
        &:nth-child(3) {
          font-size: 24px;
          height: 34px;
          line-height: 34px;
          color: #999;
          white-space: nowrap;
          text-overflow: ellipsis;
          overflow: hidden;
        }
      }
    }
  }
}
</style>
