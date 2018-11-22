<template>
  <div class="content">
         <view class="header">
                <view class="success">
                  <img src="../../../../static/images/finish@2x.png" alt="">
                </view>

                <view class="status txt_center">已结算</view>
                <view class="order_id txt_center">流水号：2018111023666</view>
                <view class="count txt_center">1944.00</view>

                <ul class="des mt50">
                  <li>
                    <span class="left">收款时间：</span>
                    <span class="right">2018-11-09  13:27:24</span>
                  </li>
                  <li>
                    <span class="left">收款方式：</span>
                    <span class="right">线上收款</span>
                  </li>
                </ul>

         </view>

         <view class="details">
           <view class="title">
             <view class="left">订单详情</view>
             <view class="right"><img src="../../../../static/images/down@2x.png" alt=""></view>
           </view>

           <ul class="des">
             <li>
               <span class="left">订单日期：</span>
               <span class="right">2018-11-09</span>
             </li>
              <li>
               <span class="left">客户下单：</span>
               <span class="right">2018-11-09  20:00:48</span>
             </li>
             <li>
               <span class="left">经理抢单：</span>
               <span class="right">2018-11-09  20:01:00  （刘伟）</span>
             </li>
               <li>
               <span class="left">通话时间：</span>
               <span class="right">20:02:03-20:05:00</span>
             </li>
               <li>
               <span class="left">发送通知：</span>
               <span class="right">2018-11-09  20:05:12</span>
             </li>
               <li>
               <span class="left">付款时间：</span>
               <span class="right">2018-11-09  13:27:24</span>
             </li>
           </ul>

         <view class="doubt">对此订单有疑问？</view>

         </view>

      
     
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },

  components: {},

  methods: {},

  created() {}
};
</script>
 
 <style lang="less" scoped>
.content {
  width: 100%;
  height: 1206rpx;
  background-color: #f4f4f4;
  box-sizing: border-box;
  overflow: hidden;
  .header {
    width: 100%;
    height: 672rpx;
    background-color: #fff;
    box-sizing: border-box;
    padding-top: 78rpx;
    .success {
      width: 100%;
      height: 136rpx;
      text-align: center;
      img {
        width: 136rpx;
        height: 136rpx;
      }
    }

    .txt_center {
      text-align: center;
    }
    .status {
      font-family: PingFang-SC-Medium;
      color: rgb(0, 0, 0);
      font-size: 40rpx;
      margin-top: 60rpx;
    }
    .order_id {
      font-family: PingFang-SC-Medium;
      color: rgb(136, 136, 136);
      font-size: 30rpx;
      margin-top: 22rpx;
    }
    .count {
      font-family: PingFang-SC-Bold;
      color: #000;
      font-size: 60rpx;
      margin-top: 20rpx;
    }
    .mt50{
      margin-top: 50rpx;
    }
  }
  
  .des {
    width: 100%;
    margin-top: 35rpx;
    box-sizing: border-box;
    padding-left: 61rpx;
    li {
      width: 100%;
      .left {
        font-family: PingFang-SC-Medium;
        color: rgb(136, 136, 136);
        font-size: 28rpx;
      }
      .right {
        font-family: PingFang-SC-Medium;
        color: rgb(0, 0, 0);
        font-size: 28rpx;
        margin-left: 61rpx;
      }
    }
  }
  .details {
    width: 100%;
    height: 533rpx;
    background-color: #fff;
    margin-top: 20rpx;
    .title {
      width: 100%;
      height: 88rpx;
      line-height: 88rpx;
      box-sizing: border-box;
      padding-left: 61rpx;
      padding-right: 23rpx;
      clear: both;
      .left {
        display: block;
        float: left;
      }
      .right {
        display: block;
        float: right;
        img{
          width: 25rpx;
          height: 16rpx;
        }
      }
    }
     .doubt{
    width: 100%;
    font-family: PingFang-SC-Medium;
    color:rgb(136,136,136);
    font-size: 28rpx;
    text-align: center;
    margin-top: 30rpx;
  }
  }

 
}
</style>
 