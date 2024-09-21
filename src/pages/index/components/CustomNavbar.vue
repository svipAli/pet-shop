<script setup lang="ts">
// 获取屏幕边界到安全区域距离
// const { safeAreaInsets } = uni.getSystemInfoSync()
// console.log(safeAreaInsets)
</script>

<template>
  <view class="navbar">
    <view class="location">
      <image
        src="@/static/images/定位.png"
        mode="scaleToFill"
        style="width: 50rpx; height: 50rpx"
      />
      <div class="city">北京市</div>
    </view>
    <view class="search">
      <text class="icon-search">搜索服务</text>
    </view>
  </view>
</template>

<style lang="scss">
/* 自定义导航条 */
.navbar {
  background-size: cover;
  background-image: linear-gradient(to bottom, #ffe3b6, #ffefdb);
  display: flex;
  justify-content: space-between;
  margin-bottom: 10rpx;
  .location {
    align-items: center;
    padding: 3rpx;
    margin: 16rpx 20rpx;
    font-size: 28rpx;
    color: #101010;
    display: flex;
    justify-content: space-between;
    .city {
      margin-left: 5px;
    }
  }
  .search {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 0 10rpx 0 26rpx;
    width: 500rpx;
    height: 60rpx;
    margin: 16rpx 20rpx;
    color: #424242;
    font-size: 28rpx;
    border-radius: 32rpx;
    background-color: rgba(255, 255, 255);
    box-shadow: 1px 5px 10px #424242;
  }
  .icon-search {
    &::before {
      margin-right: 10rpx;
    }
  }
}
</style>
