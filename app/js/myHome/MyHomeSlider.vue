<template>
  <article :class="$style.article">
    <Slider :items="items" :cname="$style.slider"/>
    <section :class="$style.list">
      <div v-for="menu in menus" :key="menu.href" :class="$style.item">
        <router-link :to="{name: menu.href}">
          <img :src="menu.src" :alt="menu.title">
          <h4>{{ menu.title }}</h4>
        </router-link>
      </div>
    </section>
  </article>
</template>

<script>
import Slider from "../core/Slider.vue"
export default {
  name: "MyHomeSlider",
  components: { Slider },
  data() {
    return {
      items: [
        {
          href: "item1",
          src: "//img20.360buyimg.com/mcpageview/jfs/t1/106678/1/12210/92914/5e4535daE1770d4c3/30137746303353c1.jpg"
        },
        {
          href: "item2",
          src: "//img20.360buyimg.com/mcpageview/jfs/t1/122349/17/1613/199131/5ebe417bE9608b120/2d1eafa4647e5801.jpg"
        },
        {
          href: "item3",
          src: "//img20.360buyimg.com/mcpageview/jfs/t1/93607/27/9768/38387/5e11d688E04270824/2d9495f7de2365ca.jpg"
        },
      ],
      menus: [
        {
          href: "menu1",
          src: "//img20.360buyimg.com/mcpageview/jfs/t1/101844/12/9760/11216/5e11d703Ec915a9b9/014b4c8a90f4f970.png",
          title: "优惠券",
        },
        {
          href: "menu2",
          src: "//img20.360buyimg.com/mcpageview/jfs/t1/90523/1/9767/16031/5e11d735E29291893/7ea1474e22f075a3.png",
          title: "领钢镚",
        },
        {
          href: "menu3",
          src: "//img20.360buyimg.com/mcpageview/jfs/t1/94998/29/9746/11665/5e11d753E53811340/b555a3fb637dad6d.png",
          title: "白条提额",
        },
        {
          href: "menu4",
          src: "//img20.360buyimg.com/mcpageview/jfs/t1/105209/4/9857/12579/5e11d770E4e458bc7/fbbbec1918b041e3.png",
          title: "领京豆",
        },
        {
          href: "menu5",
          src: "//img20.360buyimg.com/mcpageview/jfs/t1/95010/16/9777/10019/5e11d791E1d2871b3/66a53d1849c687e7.png",
          title: "工资理财",
        },
        {
          href: "menu6",
          src: "//img20.360buyimg.com/mcpageview/jfs/t1/101963/37/9857/11372/5e11d7a7E05793a8e/f9371aee1e18ae9a.png",
          title: "京东众筹",
        },
        {
          href: "menu7",
          src: "//img20.360buyimg.com/mcpageview/jfs/t1/90523/1/9767/16031/5e11d735E29291893/7ea1474e22f075a3.png",
          title: "1元扭蛋机",
        },
        {
          href: "menu8",
          src: "https://img20.360buyimg.com/mcpageview/jfs/t1/85137/14/9816/10770/5e11d7ddE2805969c/9f4f3cdcfeb204e5.png",
          title: "免息红包",
        },
      ],
    }
  },
}
</script>

<style lang="scss" module>
@import "../../css/element.scss";
.article{
  background-color: white;
  .slider{
    img{
      width: 100%;
      height: 400px;
    }
  }
  .list {
    @include list(row);
    background-color: #fff;
    justify-content: space-around;
    margin-top: 20px;

    a {
      text-decoration: none;
    }

    .item {
      text-align: center;
      width: 200px;
      height: 170px;
      margin-bottom: 50px;

      img {
        width: 112.5px;
        height: 112.5px;
      }

      h4 {
        font-size: 32.5px;
        color: #666;
        margin-top: 15px;
        overflow: hidden;
      }
    }
  }
}

</style>
