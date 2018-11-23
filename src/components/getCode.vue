<template>
   <div class="content">
          <view class="getCode" v-show="!isGetCode" @click="getCode">获取验证码</view>
          <view class="getCode active" v-show="isGetCode">倒计时{{time}}s</view>
   </div>
</template>

<script>
export default {
  data() {
    return {
      isGetCode: false,
      time: 60
    };
  },
  props:['phoneNum'],
  methods: {
    // 获取验证码
    getCode() {
      var that = this;
      console.log(that.phoneNum,'===手机号=====');
      that.isGetCode = true;
      var timer = setInterval(() => {
        that.time--;
        if (that.time < 0) {
          that.isGetCode = false;
          clearInterval(timer);
          that.time = 60;
        }
      }, 1000);
    }
  }
};
</script>

 <style lang="less" scoped>
.content {
  .getCode {
    float: right;
    width: 168rpx;
    height: 60rpx;
    border: 1px solid rgb(26, 173, 25);
    color: rgb(26, 173, 25);
    font-family: PingFang-SC-Regular;
    font-size: 26rpx;
    text-align: center;
    line-height: 60rpx;
    border-radius: 6rpx;
    margin-top: 25rpx;
    margin-right: 42rpx;
  }

  .active {
    color: rgb(191, 191, 191);
    border: 1px solid rgb(191, 191, 191);
  }
}
</style>
 
