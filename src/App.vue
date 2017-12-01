<template>
  <div id="app">
    <v-header></v-header>
    <searchlables></searchlables>
    <div class="selected"></div>
    <div class="content">
      <div class="map">
        <img src="http://placehold.it/575x689"/>
      </div>
      <div class="places">
        <div class="places-header">
          <div class="all">共<span class="num">321</span>个景点</div>
          <div class="sort-type">
            <span class="tab-item hot">
              热度排行
            </span>
            <span class="tab-item ratings">
              好评排行
            </span>
          </div>
        </div>
        <div class="place-wrapper">
          <place></place>
          <place></place>
          <place></place>
          <place></place>
          <place></place>
          <place></place>
          <place></place>
          <place></place>
        </div>
      </div>
      <div class="scenes"></div>
    </div>
  </div>
</template>

<script type="text/ecmascript-6">
  import header from './components/header/header.vue';
  import searchlables from './components/searchlable/searchlable.vue';
  import place from './components/place/place.vue';

  export default{
    components: {
      'v-header': header,
      'searchlables': searchlables,
      place
    }
  };
</script>

<style lang="stylus" rel="stylesheet/stylus">
  .selected
    width: 1440px
    height: 4px
    background: #768C7F
  .content
    font-size: 0px
    width: 1440px
    .map
      display: inline-block
    .places
      display: inline-block
      width: 632px
      height: 689px
      overflow: hidden
      .places-header
        font-size: 14px
        letter-spacing: 0
        .all
          margin-left: 17px
          margin-top: 11px
          color: #CCCCCC;
          .num
            color: #2A2A2A;
            line-height: 20px
            font-size: 16px
            padding: 0 4px
        .sort-type
          margin-left: 453px
          margin-top: -24px
          display: flex
          border: 1px solid #CCCCCC
          border-radius: 5px
          line-height: 23px
          width: 161px
          height: 23px
          .tab-item
            flex: 1
            font-size: 12px
            text-align: center
          .hot
            border-right: 1px solid #CCCCCC
            color: #666666
          .ratings
            color: #CCCCCC
      .place-wrapper
        margin-left: 7px
    .scenes
      display: inline-block
      width: 233px
      height: 689px
      background:  rgba(173,213,186,0.20)
</style>
