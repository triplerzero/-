<template>
  <div class="Swiper">
    <div class="SwiperItem" :style="{height:config.height,width:config.width,containerStyle}">
      <div v-for="(item,index) in config.items" class="SwiperItems">
        <img :src="item.img" alt="">
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Swiper',
  data () {
    return {
     config:{
       height:"400px",
       width:"400px",
       items:[
         {
           img:"http://cdn.dev.terran.wxpai.cn/upload/dev/49f0210d-09b4-4229-9af1-6044af1275b2.png"
         },
         {
           img:"http://thirdwx.qlogo.cn/mmopen/vi_32/DMaBplJOKkUHk6Mu2DVD8SWaboibJjbeCAySR7NECm1mfolyEyvSSW8UzUJZ8HlkhwD4ibd3cbd35to2QX1mOtYg/132"
         },
         {
           img:"http://cdn.dev.terran.wxpai.cn/upload/dev/757cffad-9972-46e7-a35c-0c0b86ca1ab2.jpg "
         }
       ],
     }
    }
  },
  computed:{
    containerStyle() {
      return {
        transform:`translate3d(${this.config.width}px, 0, 0)`
      }
    }

  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .SwiperItem{
    position: relative;
  }

  .SwiperItems{
    position: absolute;
  }
  .SwiperItems img{
    height: 100%;
    width: 100%;
  }
</style>
