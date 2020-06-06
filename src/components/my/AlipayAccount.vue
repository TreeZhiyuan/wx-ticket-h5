<template>
  <div>
    <group title="请完善您的付款信息" label-width="4.5em" label-margin-right="2em" label-align="right">
      <x-input title="收款方式" disabled value="支付宝"></x-input>
      <x-input title="真实姓名" placeholder="请输入支付宝真实姓名" v-model="realName"></x-input>
      <x-input title="收款账号" placeholder="请输入支付宝收款账号" v-model="alipay">
        <x-icon slot="right" type="ios-information-outline" v-on:click="showInformation"></x-icon>
      </x-input>
    </group>
    <group title="请完善通知信息" label-width="4.5em" label-margin-right="2em" label-align="right">
      <x-input title="手机号码" name="mobile" placeholder="请输入手机号码"
               keyboard="number" v-model="mobile" is-type="china-mobile"></x-input>
      <x-input title="Email" name="email" placeholder="请输入电子邮箱地址"
               is-type="email" v-model="email"></x-input>
    </group>
    <br/>
    <toast v-model="show8" type="text" width="15rem" text="<span style='font-size:12px'>支付宝 > 我的 > 个人信息 > 支付宝账号</span>"></toast>
    <div style="padding:0 25px;">
      <x-button :text="submit001" style="border-radius:99px;"
                @click.native="processButton001" type="primary"></x-button>
    </div>
  </div>
</template>

<script>
    import {
        Toast,
        GroupTitle,
        Group,
        Cell,
        XInput,
        XButton,
        Selector,
        PopupPicker,
        Datetime,
        XNumber,
        ChinaAddressData,
        XAddress,
        XTextarea,
        XSwitch
    } from 'vux'

    export default {
        name: "AlipayAccount",
        components: {
            Group,
            GroupTitle,
            Cell,
            XButton,
            XInput,
            Selector,
            PopupPicker,
            XAddress,
            Datetime,
            XNumber,
            XTextarea,
            XSwitch,
            Toast
        },
        data() {
            return {
                addressData: ChinaAddressData,
                addressValue: ['广东省', '深圳市', '南山区'],
                realName: '',
                alipay: '',
                value2: '支付宝',
                email: '',
                mobile: '',
                value3: '',
                value7: '',
                value8: '',
                submit001: '提交',
                time1: '2017-06-01',
                value5: ['A'],
                value6: [],
                list: [['A', 'B', 'C']],
                numberValue: 0,
                show8:false
            }
        }, methods: {
            showInformation: function () {
                this.show8 = true
            },
            processButton001: function () {

            }
        }
    }
</script>

<style scoped>

</style>
