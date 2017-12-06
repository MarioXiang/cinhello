<template>
  <baidu-map ref="map" class="map" :center="cityName" :scroll-wheel-zoom="true" ak="d8EKHvxx6qi2H4CfneivlDIwS3CGujMX">
    <bm-navigation anchor="BMAP_ANCHOR_TOP_LEFT"></bm-navigation>
    <bm-marker :position="{lng: 106.553835, lat: 29.556178}" :icon="{url: './src/components/map/location.png', size: {width: 20, height: 20}}" @click="infoWindowOpen">
      <bm-info-window class="info" :height="0" :width="0" :show="ifShow" @close="infoWindowClose" @open="infoWindowOpen">
        <img style="margin: 13px 14px 10px 14px" src="http://placehold.it/248x140">
        <div style="text-align: start;">
          <span style="padding-left: 13px; line-height: 25px;font-family: PingFangSC-Light; font-size: 18px; color: #333333; letter-spacing: 0;">古木屋</span>
          <span style="padding-left: 101px; line-height: 25px; font-family: PingFangSC-Light; font-size: 12px; color: dimgray;">11 收藏   3 拍过 </span>
        </div>
      </bm-info-window>
    </bm-marker>
  </baidu-map>
</template>

<script type="text/ecmascript-6">
  import place from '../place/place.vue';

  export default {
    props: {
      cityName: {
        type: String,
        default: '重庆'
      }
    },
    data () {
      return {
        ifShow: false
      };
    },
    methods: {
      infoWindowClose () {
        this.ifShow = false;
      },
      infoWindowOpen () {
        this.ifShow = true;
      }
    },
    components: {
      place
    }
  };
</script>

<style lang="stylus" rel="stylesheet/stylus">
  .map
    height: 100%
</style>
