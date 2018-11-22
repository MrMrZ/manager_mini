<template>
  <div class="content">
       

        <div class="msg ">
          <div class="title">交易提醒</div>
          <div class="details">您的微信钱包于2018年11月21日17:47:00已收入人民币3.000.00元。点击查看详情。</div>
        </div>
        <div class="msg ">
          <div class="title">系统消息</div>
            <div class="details">您的微信钱包于2018年11月21日17:47:00已收入人民币3.000.00元。点击查看详情。</div>

        </div>
        <div class="msg ">
          <div class="title">系统消息</div>
          <div class="details">您于2018年10月20日21:57:00反馈的问题我们已经收到并回复了，点击查看详情。</div>
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
   height: 1206rpx;
   background-color: #f4f4f4;
   box-sizing: border-box;
border: 1px solid #f4f4f4;

  // 消息
  .msg{
    width: 100%;
    height: 172rpx;
    background-color: #fff;
    box-sizing: border-box;
    padding-top:20rpx ;
    padding-left: 32rpx;
    margin-top: 30rpx;

    .title{
      font-family: PingFang-SC-Medium;
      font-size: 34rpx;
      color:#000;
    }
    .details{
       font-family: PingFang-SC-Regular;
      font-size: 26rpx;
      color:rgb(106,106,106);
      margin-top: 16rpx;
    }
  }
  .mt30{
    margin-top: 30rpx;
  }
 }
 </style>
 