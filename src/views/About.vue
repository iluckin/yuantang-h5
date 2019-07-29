<template>
  <div class="header">
    <Carousel class="banner-box"
            v-model="banner.value3"
            :autoplay="banner.setting.autoplay"
            :autoplay-speed="banner.setting.autoplaySpeed"
            :dots="banner.setting.dots"
            :radius-dot="banner.setting.radiusDot"
            :trigger="banner.setting.trigger"
            :arrow="banner.setting.arrow">
      <CarouselItem v-for="b in banner.items" v-bind:key="b.link">
        <div class="demo-carousel">
          <img class="banner-item" v-bind:src="b.image" alt="b.title">
        </div>
      </CarouselItem>
    </Carousel>
  </div>
</template>
<style>
  .header {
    /*margin-top: 160px;*/
    margin-top: 15px;
    margin-bottom: 15px;
  }
 .banner-item {
    height: 160px;
    width: 100%;
  }
</style>
<script>
    export default {
        data () {
            return {
                banner: {
                    value3: 0,
                    setting: {
                        autoplay: true,
                        autoplaySpeed: 2000,
                        dots: 'inside',
                        radiusDot: false,
                        trigger: 'click',
                        arrow: false
                    },
                    items: [
                        {
                            'image': 'http://deed.static.wowphp.cn/images/banners/20190725/hO1hVyU3U5zUjiqkOgX1ubt3H0QTfEEA0XD3uH8H.jpeg',
                            'link': '/',
                            'name': 'one',
                            'title': 'nice'
                        },
                        {
                            'image': 'http://deed.static.wowphp.cn/images/banners/20190725/B5d390ff8daac9.jpg',
                            'link': '/',
                            'name': 'one',
                            'title': 'nice'
                        },
                        {
                            'image': 'http://deed.static.wowphp.cn/640.jpeg',
                            'link': '/',
                            'name': 'one',
                            'title': 'nice'
                        }
                    ]
                }
            }
        }
    }
</script>

