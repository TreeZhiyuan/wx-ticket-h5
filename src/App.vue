<template>
  <div id="app">
    <ViewBox>
      <router-view></router-view>
    </ViewBox>
    <HomeTabbar></HomeTabbar>
  </div>
</template>

<script>
    import HomeTabbar from "./components/HomeTabbar";
    import {ViewBox} from 'vux'

    export default {
        name: 'app',
        components: {HomeTabbar, ViewBox}
    }
</script>

<style lang="less">
  @import '~vux/src/styles/reset.less';

  body {
    background-color: #fbf9fe;
  }
</style>
