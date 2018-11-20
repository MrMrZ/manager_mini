<template>
  <div class="content">
        <div class="total_count">
            <div class="money">
              <span class="rmb">&yen;</span>
              <span class="number">1,5000.00</span>
            </div>
            <div class="des">本月流水净收入</div>
        </div>

        <div class="info">通知</div>

        <div class="msg">
          <div class="title">交易提醒</div>
          <div class="details">您的微信钱包已收入人民币3.000.00元。点击查看详情。</div>
        </div>
        <div class="msg mt30">
          <div class="title">系统消息</div>
          <div class="details">您反馈的问题我们已收到，点击查看回复内容。</div>
        </div>
        <div class="msg mt30">
          <div class="title">系统消息</div>
          <div class="details">您反馈的问题我们已收到，点击查看回复内容。</div>
        </div>
  </div>
</template>

<script>

export default {
  data () {
    return {
     
    }
  },

  components: {
     
  },

  methods: {
     
  },

  created () {
   
  }
}
</script>
 
 <style lang="less" scoped>
 .content{
   width: 100%;
   height: 1109rpx;
   background-color: #f4f4f4;
   box-sizing: border-box;
  //  总收入金额
   .total_count{
     width: 100%;
     height: 293rpx;
     background-color: #fff;
     box-sizing: border-box;
     padding-top: 80rpx;
     .money{
       width: 100%;
       text-align: center;
       position: relative;
       .rmb{
         position: absolute;
         top: 18rpx;
         left: 159rpx;
         font-family: PingFang-SC-Medium;
         font-size: 36rpx;
         color:#000;
       }
       .number{
         font-family: PingFang-SC-Medium;
         color:#000;
         font-size: 72rpx;
       }
     }
     .des{
       width: 100%;
       text-align: center;
       color:rgb(0,0,0);
       font-size: 28rpx;
       font-family: PingFang-SC-Medium;
       margin-top: 30rpx;
     }
   }

  //  通知
  .info{
    height:83rpx ;
    font-family: PingFang-SC-Bold;
    color:rgb(106,106,106);
    font-size: 34rpx;
    box-sizing: border-box;
    padding-top: 25rpx;
    padding-left: 35rpx;

  }

  // 消息
  .msg{
    width: 100%;
    height: 172rpx;
    background-color: #fff;
    box-sizing: border-box;
    padding-top:42rpx ;
    padding-left: 32rpx;
    .title{
      font-family: PingFang-SC-Medium;
      font-size: 34rpx;
      color:#000;
    }
    .details{
       font-family: PingFang-SC-Regular;
      font-size: 26rpx;
      color:rgb(106,106,106);
      margin-top: 24rpx;
    }
  }
  .mt30{
    margin-top: 30rpx;
  }
 }
 </style>
 