<script setup lang="ts">
import CustomNavbar from './components/CustomNavbar.vue'
import PetSwiper from '@/components/PetSwiper.vue'
import { ref } from 'vue'
import type { BannerItem } from '@/types/home'
import { getHomeBannerAPI } from '@/services/home'
import CategoryPanel from './components/CategoryPanel.vue'
import HotPanel from './components/HotPanel.vue'
import TabBar from '@/components/tabbar/TabBar.vue'

// 获取轮播图数据
const bannerList = ref<BannerItem[]>([])
const getHomeBannerData = async () => {
  const res = await getHomeBannerAPI()
  bannerList.value = res.result
}
getHomeBannerData()
// 获取分类数据
</script>

<template>
  <CustomNavbar />
  <PetSwiper :list="bannerList" />
  <CategoryPanel />
  <HotPanel />
  <TabBar :index="0" />
</template>

<style lang="scss" scoped></style>
