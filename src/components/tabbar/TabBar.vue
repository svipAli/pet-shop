<template>
  <view class="ynq-tabbar">
    <view class="ynq-tabbar-bg-box">
      <image class="ynq-tabbar-bg" src="/static/tabs/tabbar-top.png" mode="aspectFill"></image>
      <view class="ynq-mid-icon"></view>
      <view class="ynq-tabbar-box" style="z-index: 99">
        <view
          class="ynq-tabbar-item"
          v-for="(tab, index) in data"
          :key="index"
          @tap="tabbarItemClick(tab, index)"
        >
          <image
            class="ynq-tabbar-icon"
            :src="tabbarIndex == index ? tab.selectedIconPath : tab.iconPath"
            mode="aspectFill"
          >
          </image>
          <view
            class="ynq-tabbar-text"
            :class="tabbarIndex == index ? 'ynq-tabbar-text-select' : ''"
            >{{ tab.text }}
          </view>
        </view>
      </view>
    </view>
    <!-- IOS安全距离START -->
    <view class="ynq-ios-aq"></view>
    <!-- IOS安全距离END -->
  </view>
</template>

<script setup lang="ts">
import { ref, onMounted, reactive } from 'vue'
let props = defineProps(['index'])
let tabbarIndex = ref(0)
const data = reactive([
  {
    pagePath: '/pages/index/index',
    text: '首页',
    iconPath: '/static/images/主页.png',
    selectedIconPath: '/static/images/主页.png',
  },
  {
    pagePath: '/pages/category/category',
    text: '分类',
    iconPath: '/static/images/分类.png',
    selectedIconPath: '/static/images/分类.png',
  },
  {
    pagePath: '/pages/push/push',
    text: '发布',
    iconPath: '/static/images/增加.png',
    selectedIconPath: '/static/images/增加.png',
  },
  {
    pagePath: '/pages/doc/doc',
    text: '档案',
    iconPath: '/static/images/档案.png',
    selectedIconPath: '/static/images/档案.png',
  },
  {
    pagePath: '/pages/my/my',
    text: '我的',
    iconPath: '/static/images/我的.png',
    selectedIconPath: '/static/images/我的.png',
  },
])
onMounted(() => {
  tabbarIndex.value = props.index
  uni.hideTabBar()
})
function tabbarItemClick(tab: any, index: number) {
  uni.switchTab({
    url: tab.pagePath,
  })
}
</script>

<style lang="scss" scoped>
.ynq-tabbar {
  background-color: white;
  width: 100%;
  position: fixed;
  bottom: 0;
  left: 0;
  padding-bottom: calc(var(--window-bottom));
  z-index: 999;

  .ynq-ios-aq {
    height: env(safe-area-inset-bottom);
    background-color: #ffffff;
  }

  .ynq-tabbar-bg-box {
    width: 100%;
    height: 118rpx;
    position: relative;

    .ynq-tabbar-bg {
      width: 100%;
      height: 100%;
    }

    z-index: 999;

    .ynq-mid-icon {
      position: absolute;
      top: 0;
      left: 50%;
      border-radius: 100%;
      width: 92rpx;
      height: 92rpx;
      padding: 20rpx;
      z-index: 1000;
      transform: scale(0.5) translate(-98%, -35%);

      image {
        width: 100%;
        height: 100%;
        transform: scale(1.2);
      }
    }

    .ynq-tabbar-box {
      width: 100%;
      height: 96rpx;
      position: absolute;
      bottom: 0;
      left: 0;
      display: flex;

      .ynq-tabbar-item {
        flex: 1;
        height: 100%;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;

        .ynq-tabbar-icon {
          width: 46rpx;
          height: 46rpx;

          padding: 2px;
          /*  */
        }

        .ynq-tabbar-text {
          color: #999;
          margin-top: 6rpx;
          line-height: 1;
          font-size: 28rpx;
        }

        .ynq-tabbar-text-select {
          color: #ffd301;
        }
      }
    }
  }
}
</style>
