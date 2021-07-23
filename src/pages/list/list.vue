<template>
  <view class="index">
    <image :src="imgUrl" alt=""></image>
    <view @tap="navigateBack">回到上一页</view>
  </view>
</template>

<script>
import Taro from '@tarojs/taro'
import './list.less'

export default {
  data () {
    return {
      imgUrl: 'https://file.hepai.video/local/other/5aa8d50112e73a89bbfa5fb68860fe90.jpg',
      params: {}
    }
  },
  methods: {
    navigateBack () {
      Taro.navigateBack()
    }
  },
  created () {
    console.log('created', Taro.getCurrentInstance().router.params)
    this.params = Taro.getCurrentInstance().router.params
  },
  onReady () {
    console.log('onReady', Taro.getCurrentInstance().router.params)
  },
  onShow () {
    console.log('onShow', Taro.getCurrentInstance().router.params)
  }
}
</script>
