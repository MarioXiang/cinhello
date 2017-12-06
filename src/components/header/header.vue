<template>
  <div class="header">
    <div class="logo-wrapper">
      <img class="logo" height="28px" width="120px" src="./Page1.png"/>
    </div>
    <div class="logo-name">场景库</div>
    <div class="city-select">
      <i class="iconfont icon-location"></i>
      <el-select class="city-selected" @change="changeCity" v-model="currentCity" placeholder="请选择">
        <el-option
          v-for="city in cities"
          :key="city.id"
          :label="city.name"
          :value="city.name">
        </el-option>
      </el-select>
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
        cities: [],
        currentCity: ''
      };
    },
    methods: {
      changeCity: function () {
        this.$emit('changeCity', this.currentCity);
      }
    },
    mounted () {
      this.$ajax.get('/api/city').then((response) => {
        response = response.data;
        this.cities = response.cityList;
        for (var i = 0; i < this.cities.length; i++) {
//          console.log(this.cities[i]);
          if (this.cities[i].default === '1') {
            this.currentCity = this.cities[i].name;
          }
        }
      }).catch(function (err) {
        console.log(err);
      });
    }
  };
</script>

<style lang="stylus" rel="stylesheet/stylus">
  .header
    display: flex
    align-items: center
    height: 64px
    width: 100%
    background: #FFFFFF
    box-shadow: 0 2px 5px 0
    padding-left: 26px
    font-size: 0px
    letter-spacing: 0
    .logo
      margin-right: 10px
      padding-right: 10px
      border-right: 1px solid #ddd
    .logo-name
      width: 80px
      font-size: 26px
      color: #595757
    .city-select
      margin-left: 120px
      font-size: 18px
      font-family: PingFangSC-Medium
      color: #333
      .icon-location
        font-size: 22px
      .city-selected
        width: 100px
        margin-right: 30px
        .el-input__inner
          border: none
          font-size: 18px
          color: #333
    .search
      flex-shrink: 1
    .personal-center
      font-family: PingFangSC-Regular
      font-size: 16px
      text-align: right
      color: #333333
</style>
