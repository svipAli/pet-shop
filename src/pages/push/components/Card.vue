<script setup lang="ts"></script>
<template>
  <view class="card">
    <view class="avatar">
      <image
        src="https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fci.xiaohongshu.com%2F68fd5302-bd0a-146a-01af-29f5458379cf%3FimageView2%2F2%2Fw%2F1080%2Fformat%2Fjpg&refer=http%3A%2F%2Fci.xiaohongshu.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=auto?sec=1729351218&t=0ee3f7dc8873fcc4a64e48ae41fdb05a"
        mode="scaleToFill"
      />
    </view>
    <view class="main">
      <view class="nick"> 次仁巴措 </view>
      <text class="main-text" selectable="false" space="false" decode="false">
        白日依山尽，黄河入海流。欲穷千里目，更上一层楼。
      </text>
      <uni-grid :column="3" :showBorder="false">
        <uni-grid-item v-for="item in 9" :key="item">
          <image
            src="https://ww4.sinaimg.cn/mw690/0066j9Zzly1hsyvsbc338j30wr0wrk02.jpg"
            mode="scaleToFill"
            style="margin: 3px 0; max-width: 80px"
          />
        </uni-grid-item>
      </uni-grid>
      <view class="controls">
        <view class="time"> 24分钟前 </view>
        <view class="control">
          <view class="like"><uni-icons type="heart" size="14"></uni-icons>点赞 </view>
          <view class="comment"><uni-icons type="chatbubble" size="14"></uni-icons>评论 </view>
        </view>
      </view>
      <view class="interact">
        <view class="like-list nick">
          <uni-icons type="heart" size="14" color="rgb(63, 107, 172)"></uni-icons>
          晞恩
        </view>
        <view class="comment-list">
          <view class="comment-detail" v-for="item in 5" :key="item">
            <view class="nick"> 晞恩： </view>
            <text>这个头像真帅！ </text>
          </view>
        </view>
      </view>
    </view>
  </view>
  <view class="parting-line"></view>
</template>

<style scoped lang="scss">
.card {
  width: 750rpx;
  min-height: 150rpx;
  display: flex;
  // justify-content: space-between;

  .avatar {
    image {
      width: 80rpx;
      height: 80rpx;
      margin: 0 10rpx 0 50rpx;
    }
  }
  .main {
    max-width: 500rpx;
    font-size: 14px;
    .nick {
      max-width: 400rpx;
      height: 50rpx;
      color: rgb(63, 107, 172);
      font-weight: 800;
    }
    .controls {
      display: flex;
      justify-content: space-between;
      margin-bottom: 5px;

      .control {
        display: flex;
        justify-content: space-between;
        .like {
          margin-right: 5px;
        }
      }
    }
    .interact {
      background-color: #efefeffe;
      border-radius: 2px;
      padding: 2px;
      .like-list {
        margin-bottom: 2px;
      }
      .comment-list {
        .comment-detail {
          display: flex;
        }
      }
    }
  }
}
.parting-line {
  justify-content: space-between;
  width: 650rpx;
  height: 1px;
  background-color: #eeeeee;
  margin: 50rpx 0 20rpx 50rpx;
}
</style>
