<template>
  <div class="searchlables">
    <div class="searchlable1">
      <div class="typename">场景类型</div>
      <div class="detail">
        <el-checkbox-group v-model="checkList1">
          <el-checkbox label="室内"></el-checkbox>
          <el-checkbox label="室外"></el-checkbox>
        </el-checkbox-group>
      </div>
    </div>
    <div class="searchlable2">
      <div class="typename">经营方式</div>
      <div class="detail">
        <el-checkbox-group v-model="checkList1">
          <el-checkbox label="市政管辖" style="color:#999999;"></el-checkbox>
          <el-checkbox label="商业运行" style="color:#999999;"></el-checkbox>
        </el-checkbox-group>
      </div>
    </div>
    <div class="searchlable3">
      <div class="typename">适宜风格</div>
      <div class="detail">
        <el-checkbox-group v-model="checkList3" class="check">
          <el-checkbox label="现代" style="color:#999999;"></el-checkbox>
          <el-checkbox label="古装" style="color:#999999;"></el-checkbox>
          <el-checkbox label="科幻" style="color:#999999;"></el-checkbox>
          <el-checkbox label="校园" style="color:#999999;"></el-checkbox>
        </el-checkbox-group>
        <span class="more">更多<i class="el-icon-arrow-down"></i></span>
      </div>
    </div>
    <div class="searchlable4">
      <div class="typename">场景类型</div>
      <div class="detail">
        <el-checkbox-group v-model="checkList4" class="check">
          <el-checkbox label="摄影棚" style="color:#999999;"></el-checkbox>
          <el-checkbox label="办公区" style="color:#999999;"></el-checkbox>
          <el-checkbox label="餐厅" style="color:#999999;"></el-checkbox>
          <el-checkbox label="咖啡馆" style="color:#999999;"></el-checkbox>
          <el-checkbox label="公园/植物园" style="color:#999999;"></el-checkbox>
          <el-checkbox label="游乐场" style="color:#999999;"></el-checkbox>
        </el-checkbox-group>
        <span class="more">更多<i class="el-icon-arrow-down"></i></span>
      </div>
    </div>
  </div>
</template>

<script type="text/ecmascript-6">
  export default{
    data () {
      return {
        checkList1: [],
        checkList2: [],
        checkList3: [],
        checkList4: [],
        searchlables: [
          {
            name: '场景类型',
            lables: [
              '室内',
              '室外'
            ]
          },
          {
            name: '经营方式',
            lables: [
              '市政管辖',
              '商业运行'
            ]
          },
          {
            name: '适宜风格',
            lables: [
              '现代',
              '古装',
              '科幻',
              '校园',
              '惊悚',
              '爱情'
            ]
          },
          {
            name: '场景类型',
            lables: [
              '摄影棚',
              '办公区',
              '餐厅',
              '咖啡馆',
              '公园/植物园',
              '游乐场'
            ]
          }
        ]
      };
    }
  };
</script>

<style lang="stylus" rel="stylesheet/stylus">
  .searchlables
    width: 100%
    height: 127px
    background: rgba(173,213,186,0.10)
    display: flex
    justify-content: space-around
    flex-wrap: wrap
    align-content: center
    .searchlable1
      display: flex
      width: 551px
      height: 40px
      background: #FFFFFF
      line-height: 40px
      margin-bottom: 11px
      .typename
        display: inline-block
        padding-left: 13px
        font-family: PingFangSC-Light
        font-size: 14px
        color: #333333
        letter-spacing: 0
      .detail
        display: inline-block
        padding-left: 49px
    .searchlable2
      display: flex
      width: 828px
      height: 40px
      background: #FFFFFF
    .searchlable3
      display: flex
      width: 551px
      height: 40px
      background: #FFFFFF
    .searchlable4
      display: flex
      width: 828px
      height: 40px
      background: #FFFFFF
</style>
<!--.searchlable1-->
<!--display: inline-block-->
<!--width: 551px-->
<!--height: 40px-->
<!--line-height: 40px-->
<!--background: #FFFFFF-->
<!--margin: 17px 14px 11px 26px-->
<!--.typename-->
<!--display: inline-block-->
<!--padding-left: 13px-->
<!--font-family: PingFangSC-Light-->
<!--font-size: 14px-->
<!--line-height: 14px-->
<!--color: #333333-->
<!--letter-spacing: 0-->
<!--.detail-->
<!--display: inline-block-->
<!--padding-left: 49px-->
<!--.searchlable2-->
<!--display: inline-block-->
<!--width: 828px-->
<!--height: 40px-->
<!--line-height: 40px-->
<!--background: #FFFFFF-->
<!--margin: 5.5px 0px-->
<!--.typename-->
<!--display: inline-block-->
<!--padding-left: 13px-->
<!--font-family: PingFangSC-Light-->
<!--font-size: 14px-->
<!--line-height: 14px-->
<!--color: #333333-->
<!--letter-spacing: 0-->
<!--.detail-->
<!--display: inline-block-->
<!--padding-left: 49px-->
<!--.lable-->
<!--width: 16px-->
<!--height: 16px-->
<!--padding-top: 3px-->
<!--.searchlable3-->
<!--display: inline-block-->
<!--width: 551px-->
<!--height: 40px-->
<!--line-height: 40px-->
<!--background: #FFFFFF-->
<!--margin:0px 14px 0px 25px-->
<!--.typename-->
<!--display: inline-block-->
<!--padding-left: 13px-->
<!--font-family: PingFangSC-Light-->
<!--font-size: 14px-->
<!--line-height: 14px-->
<!--color: #333333-->
<!--letter-spacing: 0-->
<!--.detail-->
<!--display: inline-block-->
<!--padding-left: 49px-->
<!--.check-->
<!--display: inline-->
<!--width: 373px-->
<!--color: #999999-->
<!--.more-->
<!--padding-left: 65px-->
<!--font-family: PingFangSC-Light-->
<!--font-size: 14px-->
<!--color: #999999-->
<!--letter-spacing: 0-->
<!--.searchlable4-->
<!--display: inline-block-->
<!--width: 828px-->
<!--height: 40px-->
<!--line-height: 40px-->
<!--background: #FFFFFF-->
<!--.typename-->
<!--display: inline-block-->
<!--padding-left: 13px-->
<!--font-family: PingFangSC-Light-->
<!--font-size: 14px-->
<!--line-height: 14px-->
<!--color: #333333-->
<!--letter-spacing: 0-->
<!--.detail-->
<!--display: inline-block-->
<!--padding-left: 49px-->
<!--.check-->
<!--display: inline-->
<!--width: 373px-->
<!--.more-->
<!--padding-left: 70px-->
<!--font-family: PingFangSC-Light-->
<!--font-size: 14px-->
<!--color: #999999-->
<!--letter-spacing: 0-->
