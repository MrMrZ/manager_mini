<template>
  <div  class="content" >
         <view class="logo">
               <img src="../../../static/images/LOGO@2x.png" alt="">
         </view>
         <view class="slogan">互联助推，竭诚服务</view>

         <view class="phone_con">
              <span class="number">手机号：</span>
              <input type="number" placeholder="请输入手机号">
         </view>

         <view class="code_con">
            <view class="code">
              <input type="number" placeholder="请输入验证码">
            </view>
            <view class="getCode" v-show="!isGetCode" @click="getCode">获取验证码</view>
            <view class="getCode active" v-show="isGetCode">倒计时{{time}}s</view>

         </view>

         <view class="login_btn">登录</view>
  </div>
</template>

<script>
export default {
  data(){
    return{
        time:60, //验证码倒计时
        isGetCode:false,
    }
  },
  components: {},

  computed: {},
  methods: {
      // 获取验证码
      getCode(){
        var that = this;
        that.isGetCode = true;
        var timer = setInterval(function(){
            that.time--;
            if(that.time<0){
               that.isGetCode = false;
               clearInterval(timer);
               that.time = 60;
            }
        },1000);
      },
       // 判断是否为手机号
        isPoneAvailable(pone) {
            var myreg = /^[1][3,4,5,7,8][0-9]{9}$/;
            if (!myreg.test(pone)) {
                return false;
            } else {
                return true;
            }
        },


  }
};
</script>

 <style lang="less" scoped>
.content {
  width: 100%;
  height: 1206rpx;
  box-sizing: border-box;
  padding-top: 62rpx;
  padding-left: 85rpx;
  padding-right: 85rpx;
  .logo {
    width: 100%;
    height: 160rpx;
    text-align: center;
    img {
      width: 160rpx;
      height: 160rpx;
    }
  }
  .slogan {
    width: 100%;
    text-align: center;
    font-family: PingFang-SC-Medium;
    font-size: 30rpx;
    color: rgb(157, 31, 40);
    margin-top: 59rpx;
  }

  .phone_con {
    width: 580rpx;
    height: 88rpx;
    border-radius: 44rpx;
    border: 1px solid rgba(198, 50, 62, 0.14);
    margin-top: 122rpx;
    box-shadow: 0 0 8rpx rgba(198, 50, 62, 0.14);
    overflow: hidden;
    box-sizing: border-box;
    padding-left: 35rpx;
    .number {
      display: inline-block;
      height: 100%;
      line-height: 88rpx;
      float: left;
      font-family: PingFang-SC-Regular;
      font-size: 30rpx;
      color: rgb(51, 51, 51);
    }
    input {
      float: left;
      width: 300rpx;
      margin-top: 18rpx;
      margin-left: 42rpx;
      font-size: 30rpx;
      color: #000;
    }
  }
  input::-webkit-input-placeholder,
  textarea::-webkit-input-placeholder {
    color: rgb(191, 191, 191);
    font-size: 30rpx;
  }
  input:-moz-placeholder,
  textarea:-moz-placeholder {
    color: rgb(191, 191, 191);
    font-size: 30rpx;
  }
  input::-moz-placeholder,
  textarea::-moz-placeholder {
    color: rgb(191, 191, 191);
    font-size: 30rpx;
  }
  input:-ms-input-placeholder,
  textarea:-ms-input-placeholder {
    color: rgb(191, 191, 191);
    font-size: 30rpx;
  }
  .code_con {
    width: 580rpx;
    height: 88rpx;
    border-radius: 44rpx;
    margin-top: 40rpx;
    clear: both;
    .code {
      width: 326rpx;
      height: 88rpx;
      float: left;
      border: 1px solid rgba(198, 50, 62, 0.14);
      box-shadow: 0 0 8rpx rgba(198, 50, 62, 0.14);
      border-radius: 44rpx;
      input {
        width: 100%;
        height: 100%;
        line-height: 88rpx;
        border-radius: 44rpx;
        box-sizing: border-box;
        padding-left: 35rpx;
        font-size: 30rpx;
      }
    }
    .getCode {
      width: 225rpx;
      height: 88rpx;
      float: right;
      border: 1px solid rgba(198, 50, 62, 0.14);
      box-shadow: 0 0 8rpx rgba(198, 50, 62, 0.14);
      border-radius: 44rpx;
      line-height: 88rpx;
      font-size: 30rpx;
      color: rgb(167, 53, 61);
      font-family: PingFang-SC-Regular;
      text-align: center;
    }
    .active{
      color:rgb(191, 191, 191);
    }
  }

  .login_btn {
    width: 580rpx;
    height: 88rpx;
    text-align: center;
    line-height: 88rpx;
    background-color: rgba(169, 32, 43, 0.9);
    //  background:linear-gradient(to right, rgba(152,30,39,0.64), rgba(210,58,70,0.64),rgba(169,32,43,0.9));
    color: #fff;
    font-family: PingFang-SC-Medium;
    font-size: 36rpx;
    border-radius: 44rpx;
    margin-top: 67rpx;
    box-shadow: 1rpx 13rpx 29rpx rgba(201, 1, 1, 0.16);
  }
}
</style>
 