<template>
  <div class="header">
    <div class="logo-wrapper">
      <img class="logo" cheight="30.7px" width="124.7px" src="./Page1.png"/>
      <span class="logo-name">场景库</span>
    </div>
    <div class="location">
      <i class="el-icon-location-outline" style="width: 16px; height: 18px;"></i>
      <input type="text" @click="locationListShow = true" :value="locationName" size="4" maxlength="4">
      <div class="location-list" v-show="locationListShow">
        <div style="height: 45px; line-height: 45px">
          <span style="margin-left: 16px; font-family: PingFangSC-Light; font-size: 16px;letter-spacing: 0;">城市名称</span>
        </div>
        <ul>
          <li class="location-name" :class="{ current: item == locationName }" @click="changeLocation(item)" v-for="item in locationList">{{ item }}</li>
        </ul>
      </div>
    </div>
    <div class="search">
      <el-input
        placeholder="标签，场景名称"
        prefix-icon="el-icon-search"
        v-model="input" class="input11">
      </el-input>
    </div>
    <div class="personal-center">
      登录
    </div>
  </div>
</template>

<script type="text/ecmascript-6">
  export default{
    data() {
      return {
        input: '',
        locationListShow: false,
        locationList: [
          '北京', '上海', '重庆', '运城'
        ],
        locationName: '重庆'
      };
    },
    methods: {
      changeLocation: function (name) {
        this.locationName = name;
        this.locationListShow = false;
      }
    }
  };
</script>

<style lang="stylus" rel="stylesheet/stylus">
  .header
    height: 64px
    width: 1440px
    background: #FFFFFF
    box-shadow: 0 2px 5px 0
    font-size: 0px
    .logo-wrapper
      display: inline-block
      padding: 17.1px 0px 0px 26px
      line-height: 30.7px
      .logo
        padding-right: 10px
        vertical-align: top
      .logo-name
        padding-left: 10px
        border-left: 1px solid #989898
        font-size: 26.4px
        color: #595757
    .location
      display: inline-block
      position: relative
      padding-left: 137.3px
      font-size: 18px
      font-family: PingFangSC-Medium
      color: #333333
      line-height: 25px
      .location-list
        position: absolute;
        top: 53px
        width: 249px
        height: 185px
        background: #ffffff
        border: 1px solid #CCCCCC
        box-shadow: 0 1px 4px 0 #CCCCCC
        z-index: 2
        .location-name
          display: block
          padding-left: 16px
          line-height: 44px
          font-family: PingFangSC-Light
          font-size: 16px
          color: #3F3F3F
          letter-spacing: 0
        .current
          background: #ADD5BA
      .el-icon-location-outline
        padding-right: 8px
    .search
      display: inline-block
      vertical-align: top
      margin: 14px 0 14px 54px
      .input11
        height: 36px
        width: 440px
    .personal-center
      font-family: PingFangSC-Regular;
      float: right
      margin-top: 19px
      margin-right: 32px
      font-size: 16px
      line-height: 22px
      color: #333333;
      letter-spacing: 0
</style>
