<template>
  <view class="pushNew">
    <view class="top">
      <button class="button" type="primary">发布</button>
    </view>
    <view class="main">
      <form>
        <textarea
          name="content"
          id="content"
          cols="30"
          rows="10"
          class="content"
          placeholder="这一刻的想法..."
        ></textarea>
      </form>
      <view class="upLoadPic">
        <uni-file-picker :limit="9" title="最多选择9张图片" mode="grid" file-extname="png,jpg">
        </uni-file-picker>
      </view>
    </view>
  </view>
</template>

<script lang="ts" setup></script>

<style lang="scss" scoped>
.pushNew {
  display: flex;
  flex-direction: column;

  .top {
    margin-top: 10px;
    button {
      width: 120rpx;
      height: 60rpx;
      font-size: 16px;
      line-height: 60rpx;
      margin-left: 600rpx;
    }
  }
  .main {
    .content {
      padding: 20px;
      width: 100%;
      height: 300rpx;
    }
    .upLoadPic {
      padding: 10px;
      padding-top: 0;
    }
  }
}
</style>
