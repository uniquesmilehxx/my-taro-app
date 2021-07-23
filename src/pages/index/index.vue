<template>
  <view class="index">
    <image :src="imgUrl" alt=""></image>
    <view @tap="nextPage">跳转下一页</view>
  </view>
</template>

<script>
import Taro from '@tarojs/taro'
import './index.less'

export default {
  data () {
    return {
      imgUrl: 'https://file.hepai.video/local/other/1f61cb5f57c8e5a4ed73bf2ec58fe8df.jpg',
    }
  },
  methods: {
    nextPage () {
      Taro.navigateTo({
        url: '/pages/list/list?id=blue'
      })
    },
  },
}
</script>
