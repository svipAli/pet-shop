<script lang="ts">
export default {
  options: {
    styleIsolation: 'shared',
  },
}
</script>
<template>
  <view>
    <uni-section title="最新动态" type="line" padding titleFontSize="28rpx"></uni-section>
  </view>
  <view class="ad">
    北京大兴区法斗线下见面活动火热报名中！<br />
    用户xxx成功领养猫咪一只，时间18:00<br />
    用户xxx成功领养猫咪一只，时间18:00
  </view>
  <view>
    <uni-section title="服务中心" type="line" padding titleFontSize="28rpx"></uni-section>
  </view>
  <view class="service">
    <view class="left">
      服务流程：<br />
      &nbsp;&nbsp;&nbsp;&nbsp;·填写待服务宠物档案<br />
      &nbsp;&nbsp;&nbsp;&nbsp;·选择服务项目<br />
      &nbsp;&nbsp;&nbsp;&nbsp;·预约服务时间<br />
      &nbsp;&nbsp;&nbsp;&nbsp;·等待专业人员上门<br />
    </view>
    <view class="right">
      服务承诺：<br />
      &nbsp;&nbsp;&nbsp;&nbsp;·宠托师保障<br />
      &nbsp;&nbsp;&nbsp;&nbsp;·全程可监控<br />
      &nbsp;&nbsp;&nbsp;&nbsp;·随时可沟通<br />
    </view>
  </view>
</template>

<style lang="scss">
::v-deep .uni-section .uni-section-header__decoration.line {
  width: 4px;
  height: 18px;
  border-radius: 10px;
}
.uni-section .uni-section-header__decoration {
  margin-right: 6px;
  background-color: #ffc76d;
}
.uni-section-content {
  padding: 0 !important;
}
.ad {
  width: 98%;
  padding: 20rpx;
  background-color: #ffe5ba;
  border-radius: 20px;
  margin-left: 1%;
  margin-bottom: 30rpx;
}
.service {
  width: 98%;
  margin-left: 1%;
  display: flex;
  justify-content: space-between;

  .left {
    width: 48%;
    padding: 20rpx;
    background-color: #fff9e6dd;
    border-radius: 20px;
    margin-left: 1%;
    margin-bottom: 30rpx;
  }
  .right {
    width: 48%;
    padding: 20rpx;
    background-color: #fff9e6dd;
    border-radius: 20px;
    margin-left: 1%;
    margin-bottom: 30rpx;
  }
}
</style>
