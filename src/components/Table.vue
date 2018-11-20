<template>
  <div class="content">
       <div class="top">
         <div class="left">2018111023456</div>
         <div class="right">
           <span class="type">线上</span>
           <span class="point color_yellow"></span>
           <span class="status font_yellow">未结算</span>
         </div>
       </div>
       <div class="middle">
           <view class="data_wrp">
            <view class="item">
                <view class="number">2200.00</view>
                 <view  class="des">账单金额</view>
            </view>
            <view class="item">
                <view class="number">176.00</view>
                 <view  class="des">平台服务费</view>
            </view>
            <view class="item">
                <view class="number">1944.00</view>
                 <view  class="des">回款金额</view>
            </view>

           </view>
       </div>
       <div class="msg">
         <span class="point"></span>
          <span class="txt">已扣除历史待结服务费：80.00（流水号：2018111023777）</span>
       </div>
       <div class="pay_time">
         用户支付时间：2018-11-09  13:27:24
       </div>
  </div>
</template>

<script>
export default {
   data() {
    return {};
  },
}
</script>

 <style lang="less" scoped>
 .content{
   width: 100%;
   height: 382rpx;
   background-color: #fff;
   box-sizing: border-box;
   .top {
     width: 100%;
     height: 73rpx;
     box-sizing: border-box;
     overflow: hidden;
       border-bottom: 1px solid rgb(238,238,238);

     .left{
       width: 58%;
       height: 100%;
       box-sizing: border-box;
      //  padding-top: 25rpx;
      line-height: 73rpx;
       padding-left: 31rpx;
       float: left;
       font-family: PingFang-SC-Bold;
       font-size: 34rpx;
       color:rgb(11,11,11);
     }
     .right{
       width: 40%;
         height: 100%;
       box-sizing: border-box;
      //  padding-top: 25rpx;
       padding-right: 49rpx;
       float: right;
          line-height: 73rpx;
       .type{
            font-family: PingFang-SC-Medium;
            font-size: 30rpx;
            color:rgb(0,0,0);
       }
       .point{
         display: inline-block;
         width: 12rpx;
         height: 12rpx;
         border-radius: 50%;
         margin-left: 20rpx;
       }
       .color_yellow{
         background-color: rgb(255,168,0);
       }
       .color_green{
         background-color: rgb(9,187,7);
       }
       .font_yellow{
        color:rgb(255,168,0);;
       }
       .font_green{
         color:rgb(9,187,7);
       }
       .status{
         font-family: PingFang-SC-Medium;
         font-size: 30rpx;
         margin-left: 20rpx;

       }
     }
   }

   .middle{
    .data_wrp{
       height: 198rpx;
      display: flex;
      justify-content: space-around;
      .item{
        text-align: center;
        box-sizing: border-box;
        padding-top: 40rpx;
        .number{
          font-family: PingFang-SC-Regular;
          font-size: 44rpx;
          color:#000;
        }
        .des{
           font-family: PingFang-SC-Medium;
          font-size: 28rpx;
          color:rgb(43,43,43);
          margin-top: 20rpx;
        }
      }
    }
   }

   .msg{
     margin-bottom: 10rpx;
     .point{
       display: inline-block;
       width: 12rpx;
       height: 12rpx;
       background-color: rgb(9,187,7);
       border-radius: 50%;
       margin-left: 12rpx;
     }
      .txt{
        font-family: PingFang-SC-Medium;
        font-size: 22rpx;
        color:rgb(0,0,0);
        margin-left: 12rpx;
      }
   }
   .pay_time{
     width: 100%;
     height: 58rpx;
     border-top: 1px solid rgb(238,238,238);
     border-bottom: 1px solid rgb(238,238,238);
     box-sizing: border-box;
     padding-left: 34rpx;
     line-height: 58rpx;
     font-family: PingFang-SC-Medium;
     color:rgb(166,166,166);
     font-size: 24rpx;


   }
 }
 </style>
 
