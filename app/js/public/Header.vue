<template>
  <div :class="$style.header">
    <span :class="$style.left">
      <em>登录</em>&nbsp;|&nbsp;<em>注册</em>
    </span>
    <Btn :class="$style.btnDownload">App下载</Btn>
  </div>
</template>

<script>
import Btn from "../core/Btn.vue"

export default {
  name: "Header",
  components: { Btn },
}
</script>

<style lang="scss" module>
.header {
  color: #666;
  height: 100px;
  line-height: 100px;
  font-size: 32px;
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  background: #fff url(//m.jr.jd.com/spe/qyy/main/images/jr-logo.png) center center no-repeat; /* 使用图片的背景*/
  background-size: auto 50%;
  z-index: 100; /* 层级最高，防止被其他内容覆盖*/
  .left { /* 默认是在左侧，所以不用写浮动*/
    font-size: 28px;
    height: 30px;
    line-height: 30px;
    margin: 17px 0 0 18px;
  }
  .btnDownload {
    float: right; /*右浮动*/
    font-size: 24px;
    border-width: 0;
    height: 56px;
    line-height: 56px;
    min-width: 120px;
    padding: 0;
    border-radius: 4px;
    margin: 28px 24px 0 0;
  }
}
</style>
