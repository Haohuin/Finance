<template>
  <Panel :class="$style.panel" title="新手特权">
    <section :class="$style.content">
      <div :class="$style.item">
        <h4>下载App <span :class="$style.red">送888元礼包</span></h4>
        <p :class="$style.gray">新手专享</p>
        <!--此处的图片长期不会变化，因此可以直接写死，避免http请求过多-->
        <img src="//img12.360buyimg.com/jrpmobile/jfs/t10384/155/1759179594/9776/185bd062/59e5f0ebNec4cf494.png?width=100&height=100" alt="">
      </div>
      <div :class="$style.item">
        <ul>
          <li>
            <img src="//img12.360buyimg.com/jrpmobile/jfs/t4639/162/1782623297/60754/98ea03b4/58e60952N7fdb2b85.png?width=200&height=200" alt="">
            <h4 :class="$style.red">领128元新手礼包</h4>
            <p :class="$style.gray">立即开通</p>
          </li>
          <li>
            <img src="//img12.360buyimg.com/jrpmobile/jfs/t4804/179/657713323/5908/66dce262/58e6095fNd3dc3f39.png?width=100&height=100" alt="">
            <h4>打白条<span :class="$style.red">享免息</span></h4>
            <p :class="$style.gray">立即开通享豪礼</p>
          </li>
        </ul>
      </div>
    </section>
  </Panel>
</template>
<script>
import Panel from "../core/Panel.vue"
export default {
  name: "HomeNovice",
  components: { Panel },
}
</script>

<style lang="scss" module>
@import "../../css/element.scss";
.panel{
  @include panel;
  >h4{
    border-bottom: 1px solid #ddd;
  }
  .content{
    @include list(row);
    .item{
      width: 50%;
      box-sizing: border-box;
      &:first-child {
        padding: 32px 20px;
        text-align: center;
        /*利用border来画分隔线*/
        border-right: 1px solid #ddd;
        img{
          width: 132px;
          height: 132px;
          margin: 20px auto 0;
        }
      }
      h4{
        font-size: 26px;
        line-height: 40px;
      }
      .red{
        color: #f00;
      }
      .gray{
        color: #999;
        font-size: 24px;
      }
      p{
        margin-top: 6px;
      }
      ul{
        width: 100%;
        li{
          height: 144px;
          width: 100%;
          padding: 32px 28px;
          box-sizing: border-box;
          h4{ /*不换行，超出表现...*/
            white-space: nowrap;
            text-overflow: ellipsis;
            overflow: hidden;
            text-align: left;
          }
          /*画分割线*/
          &:first-child{
            border-bottom: 1px solid #ddd;
          }
          img{
            width: 80px;
            height: 80px;
            float: right;
          }
        }
      }
    }
  }
}
</style>
