<template>
  <div>
    <tabbar>
      <tabbar-item>
        <span slot="icon"><x-icon type="ios-home"></x-icon></span>
        <span slot="label">首页</span>
      </tabbar-item>
      <tabbar-item>
        <span slot="icon"><x-icon type="ios-star"></x-icon></span>
        <span slot="label">发现</span>
      </tabbar-item>
      <tabbar-item>
        <span slot="icon"><x-icon type="ios-cart"></x-icon></span>
        <span slot="label">交易</span>
      </tabbar-item>
      <tabbar-item>
        <span slot="icon"><x-icon type="ios-search"></x-icon></span>
        <span slot="label">查询</span>
      </tabbar-item>
      <tabbar-item>
        <span slot="icon"><x-icon type="ios-person"></x-icon></span>
        <span slot="label">我的</span>
      </tabbar-item>
    </tabbar>
  </div>
</template>

<script>
    import { Tabbar, TabbarItem, Group, Cell } from 'vux'

export default {
  components: {
      Tabbar,
      TabbarItem,
      Group,
      Cell
  },
  data () {
    return {
      // note: changing this line won't causes changes
      // with hot-reload because the reloaded component
      // preserves its current state and we are modifying
      // its initial state.
      msg: 'Hello World!'
    }
  }
}
</script>

<style>
</style>
