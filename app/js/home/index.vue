<template lang="html">
  <div>
    <div :class="$style.home">
      <h1>Home</h1>
    </div>
    <div>
      设计相关的内容,teetret
    </div>
  </div>
</template>
<script>
export default {
}
</script>

<style lang="scss" module>
  @import '../../css/reset.scss';
  .home{
    color: red;
    font-size: 80px;
  }
</style>
