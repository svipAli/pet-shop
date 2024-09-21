<script lang="ts" setup>
import TabBar from '@/components/tabbar/TabBar.vue'
import Card from '@/pages/push/components/Card.vue'
function pushNewPage() {
  uni.navigateTo({
    url: '/pages/pushNew/pushNew',
  })
}
</script>

<template>
  <view class="push">
    <view class="background">
      <view class="push-content-icon" @tap="pushNewPage()">
        <uni-icons type="camera-filled" size="28" color="white"></uni-icons>
      </view>
      <image
        class="bg"
        src="https://pic.netbian.com/uploads/allimg/240714/235809-1720972689c197.jpg"
        mode="'scaleToFill'"
      />
    </view>
    <view class="nick-avatar">
      <text class="nick"> 次仁巴措</text>
      <image
        class="avatar"
        src="https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fci.xiaohongshu.com%2F68fd5302-bd0a-146a-01af-29f5458379cf%3FimageView2%2F2%2Fw%2F1080%2Fformat%2Fjpg&refer=http%3A%2F%2Fci.xiaohongshu.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=auto?sec=1729351218&t=0ee3f7dc8873fcc4a64e48ae41fdb05a"
        mode="scaleToFill"
      />
    </view>
    <view class="main">
      <scroll-view scroll-y :enable-back-to-top="true" v-for="item in 10" :key="item">
        <Card />
      </scroll-view>
    </view>
  </view>
  <TabBar :index="2" />
</template>

<style lang="scss" scoped>
.background {
  // position: relative;
  .bg {
    width: 750rpx;
    height: 421rpx;
    margin-top: -28px;
  }
  .push-content-icon {
    height: 28px;
    position: absolute;
    z-index: 999;
    margin-top: 10px;
    margin-left: 660rpx;
  }
}

.nick-avatar {
  display: flex;
  justify-content: space-between;

  .nick {
    width: 200rpx;
    height: 50rpx;
    margin-left: 390rpx;
    font-size: 20px;
    color: white;
    font-weight: 800;
    margin-top: -80rpx;
  }
  .avatar {
    width: 150rpx;
    height: 150rpx;
    margin: -100rpx 10rpx 0 20rpx;
  }
}
</style>
