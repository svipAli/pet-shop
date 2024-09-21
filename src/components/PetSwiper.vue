<template>
  <swiper
    class="banner"
    :indicator-dots="true"
    :autoplay="true"
    :interval="5000"
    :duration="1000"
    circular="true"
  >
    <swiper-item v-for="item in list" :key="item.id">
      <view class="swiper-item">
        <image :src="baseURL + item.imgUrl"></image>
      </view>
    </swiper-item>
  </swiper>
</template>

<script setup lang="ts">
import type { BannerItem } from '@/types/home'
import { baseURL } from '@/utils/http'
defineProps<{
  list: BannerItem[]
}>()
</script>

<style lang="scss" scoped>
.banner {
  border-radius: 40rpx;
}

.banner,
image {
  width: 750rpx;
  height: 300rpx;
}
</style>
