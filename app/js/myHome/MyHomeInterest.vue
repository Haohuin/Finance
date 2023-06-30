<template>
  <div :class="$style.content">
    <Panel :class="$style.panel" head="精选免息">
      <section :class="$style.list">
        <div v-for="product in products" :key="product.id" :class="$style.item">
          <img :src="product.src" :alt="product.name">
          <h4>{{ product.name }}</h4>
        </div>
      </section>
    </Panel>
  </div>
</template>

<script>
import Panel from "../core/Panel.vue"
export default {
  name: "MyHomeInterest",
  components: { Panel },
  data() {
    return {
      products: [
        {
          id: "001",
          src: "//img12.360buyimg.com/n1/s300x300_jfs/t1/213028/8/23710/460885/64478153F3b8408f2/dc58c748db027248.png",
          name: "纽霸（NIUBA）苹果数据线2.4A快速充电适用Type-c华为苹果iPhone14/13/12Pro Max/XR手机充电器线 【苹果数据线】1条装",
        },
        {
          id: "002",
          src: "//img12.360buyimg.com/n1/s300x300_jfs/t1/212382/18/29551/41609/646c8bebFfb84e4f6/e7b405024082d244.jpg",
          name: "倍呵鼻毛修剪神器男女去鼻毛剪刀电动清理鼻孔剃刮毛器防水电动鼻毛修剪器 电动鼻毛器颜色随机",
        },
        {
          id: "003",
          src: "//img12.360buyimg.com/n1/s300x300_jfs/t1/223535/8/23051/374061/646c8bd6F7a5255df/253c2e43b3d05896.png",
          name: "倍呵声控小夜灯智能语音灯床头灯夜灯卧室氛围灯语言控制感应灯 智能声控灯",
        },
        {
          id: "004",
          src: "//img12.360buyimg.com/n1/s300x300_jfs/t1/94594/7/39447/75644/646c8be4F4755fb0a/02466975f4e7f4e6.jpg",
          name: " 捷博（JIEBO）灭蚊灯家用 物理灭蚊器户外商用驱蚊器电蚊香液电蚊拍蚊子诱捕灭蝇灯母婴安全客厅 捕灭蚊神器",
        },
        {
          id: "005",
          src: "//img12.360buyimg.com/n1/s300x300_jfs/t1/165446/26/34400/150446/6479b1ffF4106433a/e675649801e033f5.jpg",
          name: "捷博（JIEBO）中国风小风扇国潮风扇随身便携式手持小风扇大风力夏季神器 【国潮手持风扇】【颜色随机】",
        },
        {
          id: "006",
          src: "//img12.360buyimg.com/n1/s300x300_jfs/t1/142994/35/30751/61245/645e00a1F3983a62e/001229fcbe49c835.jpg",
          name: "诚墨手持迷你卡通风扇户外带挂绳手提风扇便携式旅行风扇学生USB电风扇便携式充电手持小风扇 领带款绿色耳朵随机",
        },
        {
          id: "007",
          src: "//img12.360buyimg.com/n1/s300x300_jfs/t1/213028/8/23710/460885/64478153F3b8408f2/dc58c748db027248.png",
          name: "雅百达迷你小风扇定制logo手持usb户外随身便携式可爱充电低噪音大风力办公学习桌面宿舍台式小电扇 旗舰版【象牙白+支架底座】 充电款",
        },
        {
          id: "008",
          src: "//img12.360buyimg.com/n1/s300x300_jfs/t1/199437/11/32994/135241/643503c7F0736e783/247acac78824dd64.png",
          name: "桌面usb小风扇迷你办公室学生宿舍床头静音小电扇桌面小型台式电风扇上班族小风扇 5寸【一档调节-蓝色】USB直插桌面风扇",
        },
        {
          id: "009",
          src: "//img12.360buyimg.com/n1/s300x300_jfs/t1/213436/39/32895/112328/648ad206Fbf2b83da/b305a29c43689121.jpg",
          name: " 飞利浦（PHILIPS）筋膜枪肌肉按摩器运动筋膜枪专业级颈膜枪按摩筋膜枪肌肉筋膜枪经膜筋膜枪按摩器节日礼物3203G 【年度新品+8mm深度按摩】",
        },
      ],
    }
  },
}
</script>

<style lang="scss" module>
@import "../../css/element.scss";
.content {
  .panel {
    @include panel(#fff);
    > h1 {
      font-size: 50px;
      margin-left: 40px;
      font-weight: 700;
      height: 125px;
      line-height: 125px;
    }
    .list{
      @include list(row);
      justify-content: space-around;
      margin: 25px;
      .item{
        padding: 10px;
        >img{
          width: 220px;
          height: 220px;
        }
        >h4{
          box-sizing: border-box;
          padding-left: 25px;
          padding-right: 25px;
          margin-bottom: 25px;
          font-size: 30px;
          word-break: break-all;
          text-overflow: ellipsis;
          display: -webkit-box;
          overflow: hidden;
          -webkit-box-orient: vertical;
          -webkit-line-clamp: 2;
          width: 220px;
        }
      }
    }
  }
}

</style>
