<template>
  <div>
    <cell is-link value-align="left">
      <Panel :list="list" :type="type"
             @on-img-error="onImgError">
      </Panel>
    </cell>
    <grid :show-lr-borders="false" :show-vertical-dividers="false">
      <grid-item :label="'待结算'">
        <x-icon slot="icon" type="ios-pie-outline"></x-icon>
      </grid-item>
      <grid-item :label="'已打款'">
        <x-icon slot="icon" type="ios-pie-outline"></x-icon>
      </grid-item>
      <grid-item :label="'纠纷中'">
        <x-icon slot="icon" type="ios-pie-outline"></x-icon>
      </grid-item>
    </grid>
    <grid :show-lr-borders="false" :show-vertical-dividers="false">
      <grid-item :label="'待审核'">
        <x-icon slot="icon" type="ios-pie-outline"></x-icon>
      </grid-item>
      <grid-item :label="'交易中'">
        <x-icon slot="icon" type="ios-pie-outline"></x-icon>
      </grid-item>
      <grid-item :label="'纠纷中'">
        <x-icon slot="icon" type="ios-pie-outline"></x-icon>
      </grid-item>
      <grid-item :label="'已关闭'">
        <x-icon slot="icon" type="ios-pie-outline"></x-icon>
      </grid-item>
      <grid-item :label="'已结算'">
        <x-icon slot="icon" type="ios-pie-outline"></x-icon>
      </grid-item>
    </grid>
    <group title=" ">
      <cell is-link>
        <span slot="icon">
          <x-icon type="ios-pie-outline"></x-icon>
        </span>
        <span slot="title" style="color:green;padding-left: 0.2rem">
          <span style="vertical-align:middle;">交易统计</span>
        </span>
      </cell>
      <cell is-link>
        <span slot="icon">
          <x-icon type="android-checkbox-outline"></x-icon>
        </span>
        <span slot="title" style="color:green;padding-left: 0.2rem">
          <span style="vertical-align:middle;">收款信息</span>
        </span>
      </cell>
      <cell is-link>
        <span slot="icon">
          <x-icon type="social-usd-outline"></x-icon>
        </span>
        <span slot="title" style="color:green;padding-left: 0.2rem">
          <span style="vertical-align:middle;">打款记录</span>
        </span>
      </cell>
      <cell is-link>
        <span slot="icon">
          <x-icon type="ios-search"></x-icon>
        </span>
        <span slot="title" style="color:green;padding-left: 0.2rem">
          <span style="vertical-align:middle;">在线咨询</span>
        </span>
      </cell>
    </group>
    <group title=" ">
      <cell is-link>
        <span slot="icon">
          <x-icon type="ios-help-outline"></x-icon>
        </span>
        <span slot="title" style="color:green;padding-left: 0.2rem">
          <span style="vertical-align:middle;">帮助反馈</span>
        </span>
      </cell>
      <cell is-link>
        <span slot="icon">
          <x-icon type="android-notifications-none"></x-icon>
        </span>
        <span slot="title" style="color:green;padding-left: 0.2rem">
          <span style="vertical-align:middle;">通知设置</span>
        </span>
      </cell>
    </group>
  </div>
</template>

<script>
    import {
        Flexbox,
        FlexboxItem,
        Divider,
        Grid,
        GridItem,
        GroupTitle,
        Cell,
        CellBox,
        CellFormPreview,
        Group,
        Badge,
        Card,
        Panel
    } from 'vux'

    export default {
        name: "MyProfile",
        components: {
            Flexbox,
            FlexboxItem,
            Divider,
            Grid,
            GridItem,
            GroupTitle,
            Group,
            Panel,
            Cell,
            CellFormPreview,
            CellBox,
            Badge,
            Card
        },
        methods: {
            onImgError(item, $event) {
                console.log(item, $event)
            }
        },
        data() {
            return {
                avatar: "https://imgtest.cloudbae.cn:37413/api/v1/image/test/user/head/10cd0015954e4176a0b3c5c810f96206.jpeg",
                type: '1',
                list: [{
                    src: 'https://imgtest.cloudbae.cn:37413/api/v1/image/test/user/head/10cd0015954e4176a0b3c5c810f96206.jpeg',
                    fallbackSrc: 'https://imgtest.cloudbae.cn:37413/api/v1/image/test/user/head/10cd0015954e4176a0b3c5c810f96206.jpeg',
                    title: '志远',
                    desc: '男',
                    url: '/alipayAccount'
                }]
            }
        }
    }
</script>
<style scoped>
</style>
