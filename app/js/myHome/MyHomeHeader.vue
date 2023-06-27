<template>
  <section :class="$style.content">
    <div :class="$style.close">
      <img src="//img20.360buyimg.com/jdphoto/s32x32_jfs/t24304/359/2532278428/1657/ed614023/5b850f6fN747fe6a5.png" alt="">
    </div>
    <div :class="$style.item">
      <img src="//img20.360buyimg.com/mcpageview/jfs/t1/57923/31/9045/27881/5d68bf7fEe7cc16d2/c6b18ff981466ce6.png" alt="">
      <h4>打开京东金融App</h4>
      <p>一站式金融服务平台</p>
    </div>
    <button :class="$style.btnDownload">立即打开</button>
  </section>
</template>

<script>
import Btn from "../core/Btn.vue"
export default {
  name: "MyHomeHeader",
  components: { Btn },
}
</script>

<style lang="scss" module>
@import "../../css/element.scss";
.content{
  top: 0;
  position: static;
  background: #232227;
  display: flex;
  overflow: hidden;
  width: 100%;
  height: 100px;
  z-index: 200;
  .close{
    float: left;
    box-sizing: border-box;
    width: 32px;
    height: 100px;
    margin-left: 12px;
    align-items: center;
    display: flex;
    img{
      width: 32px;
      height: 32px;
    }
  }
  .item{
    float:left;
    h4{
      font-size: 24px;
      line-height: 24px;
    }
    p{
      font-size: 24px;
      line-height: 24px;
    }
    img{
      width: 70px;
      height: 100px;
    }
  }
  .btnDownload{
    float: right;
  }
}

</style>
