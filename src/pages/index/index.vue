<template>
  <div class="content">
        <div class="total_count">
            <div class="money">
              <span class="rmb">&yen;</span>
              <span class="number">{{total}}</span>
            </div>
            <div class="des">本月流水净收入</div>
        </div>

        <div class="info">通知</div>

        <div class="msg" :class="{'mt30':index!=0}"  v-for="(item,index) in lists" :key="item.id" @click="toDetails()">
          <div class="title">{{item.type}}</div>
          <div class="details">{{item.des}}</div>
        </div>

    
  </div>
</template>

<script>

export default {
  data() {
    return {
      total: "3,5000.00",
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
    };
  },

  components: {
    
  },

  methods: {
    // 消息详情
    toDetails(){
      wx.navigateTo({
            url:'../message/details/main'
      })
    }
  },

  created() {}
};
</script>
 
 <style lang="less" scoped>
.content {
  width: 100%;
  height: 1109rpx;
  background-color: #f4f4f4;
  box-sizing: border-box;
  //  总收入金额
  .total_count {
    width: 100%;
    height: 293rpx;
    background-color: #fff;
    box-sizing: border-box;
    padding-top: 80rpx;
    .money {
      width: 100%;
      text-align: center;
      position: relative;
      .rmb {
        position: absolute;
        top: 18rpx;
        left: 159rpx;
        font-family: PingFang-SC-Medium;
        font-size: 36rpx;
        color: #000;
      }
      .number {
        font-family: PingFang-SC-Medium;
        color: #000;
        font-size: 72rpx;
      }
    }
    .des {
      width: 100%;
      text-align: center;
      color: rgb(0, 0, 0);
      font-size: 28rpx;
      font-family: PingFang-SC-Medium;
      margin-top: 30rpx;
    }
  }

  //  通知
  .info {
    height: 83rpx;
    font-family: PingFang-SC-Bold;
    color: rgb(106, 106, 106);
    font-size: 34rpx;
    box-sizing: border-box;
    padding-top: 25rpx;
    padding-left: 35rpx;
  }

  // 消息
  .msg {
    width: 100%;
    height: 172rpx;
    background-color: #fff;
    box-sizing: border-box;
    padding-top: 20rpx;
    padding-left: 32rpx;
    .title {
      font-family: PingFang-SC-Medium;
      font-size: 34rpx;
      color: #000;
    }
    .details {
      font-family: PingFang-SC-Regular;
      font-size: 26rpx;
      color: rgb(106, 106, 106);
      margin-top: 16rpx;
    }
  }
  .mt30 {
    margin-top: 30rpx;
  }
}
</style>
 