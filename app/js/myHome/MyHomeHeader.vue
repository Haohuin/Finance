<template>
  <div :class="$style.content">
    <div :class="$style.close">
      <img src="//img20.360buyimg.com/jdphoto/s32x32_jfs/t24304/359/2532278428/1657/ed614023/5b850f6fN747fe6a5.png" alt="">
    </div>
    <div :class="$style.item">
      <img src="//img20.360buyimg.com/mcpageview/jfs/t1/57923/31/9045/27881/5d68bf7fEe7cc16d2/c6b18ff981466ce6.png" alt="">
      <h4>打开京东金融App</h4>
      <p>一站式金融服务平台</p>
    </div>
    <button :class="$style.btnDownload">立即打开</button>
  </div>
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
  /*fixed布局中的width:100%方法*/
  //position: fixed;
  top: 0;
  left: 0;
  right: 0;
  background: #232227;
  overflow: hidden;
  height: 125px;
  line-height: 125px;
  /*防止Header被覆盖的方法*/
  z-index: 100;
  .close{
    float: left;
    box-sizing: border-box;
    width: 40px;
    height: 125px;
    margin-left: 13.5px;
    align-items: center;
    display: flex;
    img{
      width: 40px;
      height: 40px;
    }
  }
  .item{
    margin-top: 15px;
    box-sizing: border-box;
    display: block;
    img{
      display: flex;
      float:left;
      width: 70px;
      height: 70px;
      margin-left: 20px;
      margin-right: 10px;
    }
    h4{
      color: white;
      font-size: 30px;
      line-height: 30px;
    }
    p{
      margin-top: 12px;
      color: #999;
      font-size: 30px;
      line-height: 30px;
    }
  }
  .btnDownload{
    box-sizing: border-box;
    float: right;
    color: #fff;
    text-align: center;
    line-height: 100px;
    height: 125px;
    width: 200px;
    border-width: 0;
    background: #ce2626;
    margin-top: -76px;
    overflow: hidden;
  }
}

</style>
