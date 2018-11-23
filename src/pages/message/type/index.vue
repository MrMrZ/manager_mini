<template>
  <div class="content" >
      
      <view class="title">
                  <view class="left">消息类型</view>
          </view>
       <div class="section">
         <ul>
           <li @click="toMsg()">
             <div class="left">
               交易提醒
             </div>
             <div class="right">
                <img src="../../../../static/images/next@2x.png" alt="">
             </div>
           </li>
           <li class="mt30" @click="toMsg()">
             <div class="left">
               系统消息
             </div>
             <div class="right">
                <img src="../../../../static/images/next@2x.png" alt="">
             </div>
           </li>
      
         </ul>
       </div>
  </div>
</template>

<script>
import { formatTime } from "@/utils/index";

export default {
  components: {},

  data() {
    return {};
  },
   methods:{
       

        // 消息列表管理
        toMsg(){
           wx.navigateTo({
            url:'../lists/main'
          })
        },
      


   },

  created() {}
};
</script>

 <style lang="less" scoped>
.content {
  height: 1109rpx;
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
      font-family: AdobeHeitiStd-Regular ;
      font-size: 28rpx;
      color:  rgb(136,136,136);
      box-sizing: border-box;
      padding-left: 32rpx;
    }
   }
  //  中间内容
  .section {
    width: 100%;
    border-top: 1rpx solid rgb(229, 229, 229);
    background-color: #f4f4f4;
    ul {
      .mt30 {
        margin-top: 30rpx;
      }
      li {
        width: 100%;
        height: 88rpx;
        overflow: hidden;
        box-sizing: border-box;
        padding-left: 30rpx;
        padding-right: 30rpx;
        background-color: #fff;
        .left {
          float: left;
          line-height: 88rpx;
          font-family: PingFang-SC-Medium;
          font-size: 36rpx;
          color: #000;
        }
        .right {
          float: right;
          line-height: 88rpx;
          img {
            width: 16rpx;
            height: 26rpx;
          }
          .btn {
            width: 104rpx;
            height: 74rpx;
          }
        }
      }
    }
  }
}
</style>
 