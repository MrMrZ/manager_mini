<template>
  <div  class="content" >
       <!-- 有人 -->
       <view class="has_person" v-show="true">
        
          <view class="title">
                  <view class="left">当前微信收款账号：1个</view>
                  <view class="right"> <span class="add_icon">+</span> <span>新增</span></view>
          </view>

          <!-- 授权人信息 -->
          <view class="msg_con">
            <view class="message">
              <img src="../../../../static/images/wechat@2x.png" alt="">
              <view class="main">主卡</view>
          </view>
          </view>


            <!-- 有人 -->
          <view class="title mt30">
                  <view class="left">当前公司收款账号：1个</view>
                  <view class="right"> <span class="add_icon">+</span> <span>新增</span></view>
          </view>

          <!-- 授权人信息 -->
          <view class="msg_con">
              <view class="message">
                <img src="../../../../static/images/zhaoshang@2x.png" alt="">
                  <view class="number">**** **** **** 0223</view>
            </view>
          </view>
       </view>


        <!-- 没人 -->
       <view class="no_person" v-show="false">

         <view class="title">
                  <view class="left">当前微信收款账号：无</view>
          </view>

          <!-- 授权人信息 -->
          <view class="message new">
                <span class="new_add">+</span>
                <span class="add_txt">新增</span>
          </view>

          
         <view class="title">
                  <view class="left">当前公司收款账号：无</view>
          </view>

          <!-- 授权人信息 -->
          <view class="message new">
                <span class="new_add">+</span>
                <span class="add_txt">新增</span>
          </view>

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
    background-color: #fff;
    .left {
      height: 100%;
      float: left;
      font-family: PingFang-SC-Bold;
      font-size: 28rpx;
      color: #000;
      box-sizing: border-box;
      padding-left: 32rpx;
    }
    .right {
      height: 100%;
      float: right;
      box-sizing: border-box;
      padding-right: 27rpx;
      color: rgb(24, 141, 24);
      font-family: PingFang-SC-Medium;
      font-size: 30rpx;
      .add_icon {
        font-size: 44rpx;
        margin-right: 25rpx;
      }
    }
  }
  .mt30{
    margin-top: 30rpx;
  }

.msg_con{
  width: 100%;
  height: 250rpx;
  background-color: #fff;
    box-sizing: border-box;
padding-left: 32rpx;
  .message {
    width: 686rpx;
    height: 220rpx;
    box-sizing: border-box;
    position: relative;
    img{
        width: 686rpx;
        height: 220rpx;
        position: absolute;
        left: 0;
        top: 0;
    }
    .main{
      width: 100rpx;
      height:44rpx ;
      background-color: #fff;
      text-align: center;
      line-height: 44rpx;
      color:rgb(76,184,72);
      font-family: PingFang-SC-Bold;
      font-size: 30rpx;
      border-radius: 6rpx;
      position: absolute;
      top: 26rpx;
      right: 31rpx;
    }
    .number{
      font-family: PingFang-SC-Medium;
      color:#fff;
      font-size: 49rpx;
      position: absolute;
      left: 114rpx;
      top: 107rpx;
    }
   
  }
}

  .new{
     text-align: center;
     line-height: 110rpx;
     font-family: AdobeHeitiStd-Regular;
     color:rgb(26,173,25);
     font-size: 36rpx;
     .new_add{
       font-size: 50rpx;
       margin-right: 23rpx;
     }
  }
}
</style>
 