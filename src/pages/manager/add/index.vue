<template>
  <div  class="content" >
       <!-- 有人 -->
       <view class="has_person" v-show="false">
        
          <view class="title">
                  <view class="left">当前授权经理：1人</view>
                  <view class="right"> <span class="add_icon">+</span> <span>新增</span></view>
          </view>

          <!-- 授权人信息 -->
          <view class="message">
                <view class="headimg"><img src="../../../../static/images/user1@2x.png" alt=""></view>
                <view class="username">彭于晏</view>
          </view>


            <!-- 有人 -->
          <view class="title">
                  <view class="left">当前授权财务：1人</view>
                  <view class="right"> <span class="add_icon">+</span> <span>新增</span></view>
          </view>

          <!-- 授权人信息 -->
          <view class="message">
                <view class="headimg"><img src="../../../../static/images/user1@2x.png" alt=""></view>
                <view class="username">张艺兴</view>
          </view>
       </view>


        <!-- 没人 -->
       <view class="no_person">

         <view class="title">
                  <view class="left">当前授权经理：0人</view>
          </view>

          <!-- 授权人信息 -->
          <view class="message new">
                <span class="new_add">+</span>
                <span class="add_txt">新增</span>
          </view>

          
         <view class="title">
                  <view class="left">当前授权财务：0人</view>
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

  .message {
    width: 100%;
    height: 110rpx;
    background-color: #fff;
    box-sizing: border-box;
    clear: both;
    // 有人
    .headimg {
      width: 92rpx;
      height: 100%;
      float: left;
      box-sizing: border-box;
      padding-top: 20rpx;
      padding-left: 22rpx;
      img {
        width: 70rpx;
        height: 70rpx;
      }
    }
    .username {
      width: 60%;
      height: 100%;
      line-height: 110rpx;
      float: left;
      color: #000;
      font-family: PingFang-SC-Medium;
      font-size: 36rpx;
      margin-left: 23rpx;
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
 