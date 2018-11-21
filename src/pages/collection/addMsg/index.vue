<template>
  <div  class="content" >
    
       <view class="has_person" >
          <view class="title">
                  <view class="left">请输入公司银行卡账号 </view>
          </view>

        <view class="modify">
            <!-- 卡号 -->
           <view class="phone_con">
                <view class="phone">卡号</view>
                <view class="input_phone"> <input type="number" ></view>
           </view>

          <view class="title edit">
                  <view class="left">公司信息</view>
          </view>
           <!-- 公司信息 -->
           <view class="phone_con">
                <view class="phone">开户公司名</view>
                <view class="input_phone"> <input type="number" placeholder="请输入开户公司名"></view>
           </view>
  <view class="phone_con">
                <view class="phone">开户行</view>
                <view class="input_phone"> <input type="number" placeholder="请选择开户行"></view>
           </view>
                <view class="title edit mt40">
                  <view class="left">  <checkbox   checked="true" class="w24"/>已阅读并同意 <span class="blue">《借款额度合同及相关授权》</span> </view>
          </view>

        </view>


        <view class="sure">下一步</view>

       </view>




  </div>
</template>

<script>
export default {
  components: {},

  computed: {},
  methods: {}
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
      font-family: PingFang-SC-Medium;
      font-size: 28rpx;
      color: rgb(136, 136, 136);
      box-sizing: border-box;
      padding-left: 32rpx;
    }
    checkbox {
      width: 24rpx;
      height: 24rpx;
    }
    .w24 {
      width: 24rpx;
      margin-right: 40rpx;
    }
    .blue {
      color: rgb(106, 127, 166);
    }
  }

  .edit {
    color: rgb(136, 136, 136);
    font-family: AdobeHeitiStd-Regular;
  }

  .mt40 {
    margin-top: 40rpx;
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
      width: 30%;
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
  }

  .sure {
    width: 690rpx;
    height: 88rpx;
    background-color: rgb(9, 187, 7);
    text-align: center;
    line-height: 88rpx;
    color: rgba(255, 255, 255, 0.3);
    border-radius: 10rpx;
    font-family: PingFang-SC-Medium;
    font-size: 36rpx;
    margin-top: 45rpx;
    margin-left: 30rpx;
  }
}
</style>
 