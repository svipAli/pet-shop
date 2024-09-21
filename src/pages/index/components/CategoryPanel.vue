<script setup lang="ts">
import { reactive } from 'vue'
const list = reactive([
  {
    id: 1,
    path: '/static/images/上门洗护.png',
    text: '上门洗护',
    link: '',
  },
  {
    id: 1,
    path: '/static/images/上门喂养.png',
    text: '上门喂养',
    link: '',
  },
  {
    id: 1,
    path: '/static/images/家庭清洁.png',
    text: '家庭清洁',
    link: '',
  },
  {
    id: 1,
    path: '/static/images/餐食定制.png',
    text: '餐食定制',
    link: '',
  },
])
</script>

<template>
  <view class="category">
    <template>
      <view class="category">
        <navigator
          class="category-item"
          hover-class="none"
          :url="item.link"
          v-for="item in list"
          :key="item.id"
        >
          <image class="icon" :src="item.path"></image>
          <text class="text">{{ item.text }}</text>
        </navigator>
      </view>
    </template>
  </view>
</template>

<style lang="scss" scoped>
/* 前台类目 */
.category {
  margin: 30rpx 0 0;
  padding: 10rpx 0;
  display: flex;
  flex-wrap: wrap;
  min-height: 128rpx;
  background-color: rgb(255, 251, 246);

  .category-item {
    margin-left: 30rpx;
    width: 150rpx;
    display: flex;
    justify-content: center;
    flex-direction: column;
    align-items: center;
    box-sizing: border-box;

    .icon {
      width: 80rpx;
      height: 80rpx;
      // opacity: 0.48;
    }

    .text {
      font-size: 26rpx;
      color: #000000c8;
      // font-weight: bold;
      margin-top: 10rpx;
    }
  }
}
</style>
