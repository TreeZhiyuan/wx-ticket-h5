<template>
  <div>
    <tabbar style="position:fixed">
      <tabbar-item>
        <span slot="icon"><x-icon type="ios-home"></x-icon></span>
        <span slot="label">首页</span>
      </tabbar-item>
      <tabbar-item>
        <span slot="icon"><x-icon type="ios-star"></x-icon></span>
        <span slot="label">发现</span>
      </tabbar-item>
      <tabbar-item link="/cart" selected>
        <span slot="icon"><x-icon type="ios-cart"></x-icon></span>
        <span slot="label">交易</span>
      </tabbar-item>
      <tabbar-item>
        <span slot="icon"><x-icon type="search"></x-icon></span>
        <span slot="label">查询</span>
      </tabbar-item>
      <tabbar-item link="/my">
        <span slot="icon"><x-icon type="ios-person"></x-icon></span>
<!--        <img slot="icon-active" src="../../assets/image/ic_nav_my_pressed.png">-->
        <span slot="label">我的</span>
      </tabbar-item>
    </tabbar>
  </div>
</template>

<script>
    import {Tabbar, TabbarItem, Group, Cell} from 'vux'

    export default {
        components: {
            Tabbar,
            TabbarItem,
            Group,
            Cell
        },
        data() {
            return {
            }
        }
    }
</script>

<style>
</style>
