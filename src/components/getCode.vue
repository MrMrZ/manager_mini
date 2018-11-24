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
  props: ["phoneNum"],
  methods: {
    // 判断是否为手机号
    isPoneAvailable(phone) {
      var myreg = /^[1][3,4,5,7,8][0-9]{9}$/;
      if (!myreg.test(phone)) {
        return false;
      } else {
        return true;
      }
    },
    // 获取验证码
    getCode() {
      var that = this;
      console.log(that.phoneNum, "===手机号=====");

      if (!that.phoneNum) {
        wx.showToast({
          title: "手机号不能为空",
          icon: "none",
          duration: 2000
        });
        return;
      }

      if (!that.isPoneAvailable(that.phoneNum)) {
        wx.showToast({
          title: "手机号格式不对",
          icon: "none",
          duration: 2000
        });
        return;
      }

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
 
