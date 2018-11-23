<template>
  <div class="content">
       

        <div class="msg " v-for="item in lists" :key="item.id" @click="toDetials()">
          <div class="title">{{item.type}}</div>
          <div class="details">{{item.des}}</div>
        </div>
       
  </div>
</template>

<script>

export default {
  data () {
    return {
       lists: [
        {
          id: 1,
          type: "交易提醒",
          des:   "您的微信钱包于2018年11月21日17:47:00已收入人民币3.000.00元。点击查看详情。"
        },
        {
          id: 2,
          type: "交易提醒",
          des: "您的微信钱包于2018年11月21日17:47:00已收入人民币3.000.00元。点击查看详情。"
        },
        {
          id: 3,
          type: "系统提醒",
          des:"您的微信钱包于2018年11月21日17:47:00已收入人民币3.000.00元。点击查看详情。"
        }
      ]
    }
  },

  components: {
     
  },

  methods: {
     toDetials(){
             wx.navigateTo({
               url:'../details/main'
           })
     }
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
 