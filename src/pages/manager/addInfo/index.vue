<template>
  <div  class="content" >
    
       <view class="has_person" >
        

        <view class="modify">
           <view class="title edit">
                  <view class="left">填写信息</view>
          </view>
             <!-- 修改手机号 -->
           <view class="phone_con">
                <view class="phone">姓名</view>
                <view class="input_phone"> <input type="number"  ></view>
           </view>
            <!-- 修改手机号 -->
           <view class="phone_con">
                <view class="phone">手机号</view>
                <view class="input_phone"> <input type="number" placeholder="请输入新手机号"></view>
           </view>

           <!-- 修改手机号 -->
           <view class="phone_con">
                <view class="phone">验证码</view>
                <view class="input_phone"> <input type="number" placeholder="填写验证码"></view>
                  <view class="getCode" v-show="!isGetCode" @click="getCode">获取验证码</view>
                <view class="getCode active" v-show="isGetCode">倒计时{{time}}s</view>
           </view>

                <view class="title edit">
                  <view class="left">请填写该手机号收到的验证码</view>
          </view>

        </view>


        <view class="sure" @click="sure()">确定</view>

       </view>



 


  </div>
</template>

<script>
export default {
  data(){
    return {
        time:60, //验证码倒计时
        isGetCode:false,
    }
  },
  components: {},

  computed: {},
  methods: {
    sure(){
      wx.navigateTo({
            url:'../addInfo/main'
      })
    },
     // 获取验证码
      getCode(){
        var that = this;
        that.isGetCode = true;
        var timer = setInterval(()=>{
            that.time--;
            if(that.time<0){
              that.isGetCode = false;
              clearInterval(timer);
              that.time = 60;
            }
        },1000)
      },
  }
};
</script>

 <style lang="less" scoped>
.content {
  width: 100%;
  height: 1206rpx;
  background-color: #f4f4f4;
  box-sizing: border-box;
  .title {
    width: 100%;
    height: 76rpx;
    box-sizing: border-box;
    line-height: 76rpx;
    clear: both;
    .left {
      height: 100%;
      float: left;
      font-family: PingFang-SC-Bold;
      font-size: 28rpx;
      color: #000;
      box-sizing: border-box;
      padding-left: 32rpx;
    }
  }

  .edit {
    color: rgb(136, 136, 136);
    font-family: AdobeHeitiStd-Regular;
  }

  .message {
    width: 100%;
    height: 110rpx;
    background-color: #fff;
    box-sizing: border-box;
    clear: both;
    border-bottom: 1px solid rgb(229, 229, 229);

    .username {
      width: 60%;
      height: 100%;
      line-height: 110rpx;
      float: left;
      color: #000;
      font-family: PingFang-SC-Medium;
      font-size: 36rpx;
      margin-left: 31rpx;
    }
    .select {
      height: 100%;
      float: right;
      box-sizing: border-box;
      padding-top: 20rpx;
      margin-right: 30rpx;
      img {
        width: 26rpx;
        height: 19rpx;
      }
    }
  }
  input::-webkit-input-placeholder,
  textarea::-webkit-input-placeholder {
    color: rgb(191, 191, 191);
    font-size: 33rpx;
  }
  input:-moz-placeholder,
  textarea:-moz-placeholder {
    color: rgb(191, 191, 191);
    font-size: 33rpx;
  }
  input::-moz-placeholder,
  textarea::-moz-placeholder {
    color: rgb(191, 191, 191);
    font-size: 33rpx;
  }
  input:-ms-input-placeholder,
  textarea:-ms-input-placeholder {
    color: rgb(191, 191, 191);
    font-size: 33rpx;
  }
  .phone_con {
    width: 100%;
    height: 110rpx;
    background-color: #fff;
    box-sizing: border-box;
    clear: both;
    border-bottom: 1px solid rgb(229, 229, 229);
    .phone {
      width: 26%;
      height: 100%;
      float: left;
      font-family: PingFang-SC-Medium;
      font-size: 33rpx;
      color: #000;
      box-sizing: border-box;
      padding-left: 32rpx;
      padding-top: 28rpx;
    }
    .input_phone {
      width: 40%;
      height: 100%;
      float: left;
      input {
        width: 100%;
        height: 100%;
        color: #000;
        font-size: 33rpx;
        font-family: AdobeHeitiStd-Regular;
      }
    }
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

    .active{
      color:rgb(191, 191, 191);
      border: 1px solid rgb(191, 191, 191);
    }
  }

  .sure{
    width: 690rpx;
    height:88rpx ;
    background-color: rgb(158,47,53);
    text-align: center;
    line-height: 88rpx;
    color:#fff;
    border-radius: 10rpx;
    font-family: PingFang-SC-Medium;
    font-size: 36rpx;
    margin-top: 50rpx;
    margin-left: 30rpx;
    
  }
}
</style>
 