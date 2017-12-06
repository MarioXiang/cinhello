<template>
  <div class="place">
    <div class="tags">
      <div class="tag">民国</div>
      <div class="tag">古装片</div>
      <div class="tag">可租赁</div>
    </div>
    <span class="name">古街梯</span>
    <i  class="iconfont icon-favor"></i>
    <div class="number">
      <span>11 收藏</span>
      <span>3 拍过</span>
    </div>
  </div>
</template>

<script type="text/ecmascript-6">
  export default{};
</script>

<style lang="stylus" rel="stylesheet/stylus">
  .place {
    position: relative;
    background: url("http://placehold.it/290x163") no-repeat 0 0
    width: 290px
    height: 163px
  }
  .name {
    position: absolute;
    bottom: 6.4px;
    left: 8.7px;
    font-family: PingFangSC-Medium;
    line-height: 25px;
    font-size: 18px;
    color: #FFFFFF;
    letter-spacing: 0;
  }
  .tags {
    display: inline-block;
    position: absolute;
    top: 15px;
    left: 12.8px;
    font-size: 0;
  }
  .icon-favor{
    position: absolute;
    font-size: 18px
    top: 16px;
    right: 11px;
    color: #d81e06
  }
  .tag {
    display: inline-block;
    text-align: center;
    width: 50.3px;
    height: 18.8px;
    line-height: 18.8px
    font-family: PingFangSC-Light;
    font-size: 12px;
    color: #333333;
    letter-spacing: 0;
    background: rgba(255,255,255,0.90);
    border: 1px solid #CCCCCC;
    border-radius: 5px;
    margin-right: 11.7px;
  }
  .number {
    position: absolute;
    right: 9.8px;
    bottom: 10px;
    font-family: PingFangSC-Light;
    font-size: 12px;
    color: #FFFFFF;
    letter-spacing: 0;
  }
</style>
