<template>
  <div>
    <tab :scroll-threshold="6" :line-width="2" custom-bar-width="1.5rem">
      <tab-item selected>待审核</tab-item>
      <tab-item>交易中</tab-item>
      <tab-item>纠纷中</tab-item>
      <tab-item>已关闭</tab-item>
      <tab-item>已完成</tab-item>
    </tab>
  </div>
</template>

<script>
    import { Tab, TabItem } from 'vux'
    export default {
        name: "CartDetails",
        components: {
            Tab, TabItem
        },
    }
</script>

<style scoped>

</style>
