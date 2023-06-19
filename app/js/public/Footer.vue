<template>
  <div class="header">
    <span class="left">
      <em>注册</em>&nbsp;|&nbsp;<em>登录</em>
    </span>
    <Btn class="btnDownload">App下载</Btn>
  </div>
</template>

<script>
import Btn from "../core/Btn.vue"
export default {
  name: "Footer",
  components: { Btn },
}
</script>

<style lang="scss">
  .header {
    color: #666;
    height: 100px;
    line-height: 100px;
    font-size: 32px;
    position: fixed;
    top: 0;
    background: #fff url(//m.jr.jd.com/spe/qyy/main/images/jr-logo.png) center center no-repeat; /* 使用图片的背景*/
    background-size: auto 50%;
    z-index: 100; /* 层级最高，防止被其他内容覆盖*/
    .left {
      font-size: 28px;
      height: 30px;
      line-height: 30px;
      margin: 17px 0 0 18px;
    }
    .btnDownload {
      float: right;
      font-size: 24px;
      border-width: 0;
      height: 56px;
      line-height: 56px;
      min-width: 120px;
      padding: 0;
      border-radius: 4px;
      margin: 28px ;
    }
  }
</style>
