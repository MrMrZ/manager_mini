<template>
  <div class="content">
      <div class="cont_box" :class="{'mt30':index>0}" v-for="(item,index) in lists" :key="item.id">
          <div class="top">
              <div class="left">{{item.order_id}}</div>
              <div class="right">
                <span class="type" v-if="item.type==1">线上</span>
                <span class="type" v-else-if="item.type==2">线下</span>

                <span class="point_con">
                  <span class="point color_yellow"  v-if="item.status==0"></span>
                  <span class="point color_green"  v-else-if="item.status==1"></span>

                </span>
                <span class="status font_yellow" v-if="item.status==0">未结算</span>
                <span class="status  font_green" v-else-if="item.status==1">已结算</span>

              </div>
            </div>
            <div class="middle">
                <view class="data_wrp">
                  <view class="item">
                      <view class="number">{{item.total}}</view>
                      <view  class="des">账单金额</view>
                      <span class="line"></span>

                  </view>
                  <view class="item">
                      <view class="number">{{item.server}}</view>
                      <view  class="des">平台服务费</view>
                      <span class="line"></span>

                  </view>
                  <view class="item">
                      <view class="number">{{item.real_income}}</view>
                      <view  class="des">回款金额</view>
                  </view>

                </view>
            </div>
            <div class="msg" v-show="item.type==2">
              <span class="point"></span>
                <span class="txt" >已扣除历史待结服务费：80.00（流水号：{{item.order_id}}）</span>
            </div>
            <div class="pay_time">
              用户支付时间：{{item.date}}
            </div>
       </div>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
  props:['lists']
};
</script>

 <style lang="less" scoped>
.content {
  width: 100%;
  height: 382rpx;
  box-sizing: border-box;
  .cont_box{
    background-color: #fff;
  }

  .mt30{
    margin-top: 30rpx;
  }
  .top {
    width: 100%;
    height: 73rpx;
    box-sizing: border-box;
    overflow: hidden;
    border-bottom: 1px solid rgb(238, 238, 238);
    .left {
      width: 58%;
      height: 100%;
      box-sizing: border-box;
      //  padding-top: 25rpx;
      line-height: 73rpx;
      padding-left: 31rpx;
      float: left;
      font-family: PingFang-SC-Bold;
      font-size: 34rpx;
      color: rgb(11, 11, 11);
    }
    .right {
      width: 40%;
      height: 100%;
      box-sizing: border-box;
      padding-left: 49rpx;
      float: right;
      overflow: hidden;
      .type {
        display: inline-block;
        line-height: 73rpx;
        font-family: PingFang-SC-Medium;
        font-size: 30rpx;
        color: rgb(0, 0, 0);
        float: left;
      }
      .point_con {
        display: inline-block;
        height: 73rpx;
        float: left;
        padding-top: 6rpx;
        .point {
          display: inline-block;
          width: 12rpx;
          height: 12rpx;
          border-radius: 50%;
          margin-left: 20rpx;
        }
      }

      .color_yellow {
        background-color: rgb(255, 168, 0);
      }
      .color_green {
        background-color: rgb(9, 187, 7);
      }
      .font_yellow {
        color: rgb(255, 168, 0);
      }
      .font_green {
        color: rgb(9, 187, 7);
      }
      .status {
        line-height: 73rpx;
        font-family: PingFang-SC-Medium;
        font-size: 30rpx;
        margin-left: 20rpx;
        float: left;
      }
    }
  }

  .middle {
    .data_wrp {
      height: 198rpx;
      display: flex;
      justify-content: space-around;

      .item {
        width: 33.3%;
        text-align: center;
        box-sizing: border-box;
        padding-top: 40rpx;
        position: relative;
        .number {
          font-family: PingFang-SC-Regular;
          font-size: 44rpx;
          color: #000;
        }
        .des {
          font-family: PingFang-SC-Medium;
          font-size: 28rpx;
          color: rgb(43, 43, 43);
          margin-top: 20rpx;
        }
        .line{
          display: inline-block;
          height:68%;
          width: 1rpx;
          border-right: 1px solid rgb(224,224,224);
          position: absolute;
          right: 0;
          top: 40rpx;
        }
      }
    }
  }

  .msg {
    margin-bottom: 10rpx;
    .point {
      display: inline-block;
      width: 12rpx;
      height: 12rpx;
      background-color: rgb(9, 187, 7);
      border-radius: 50%;
      margin-left: 12rpx;
    }
    .txt {
      font-family: PingFang-SC-Medium;
      font-size: 22rpx;
      color: rgb(0, 0, 0);
      margin-left: 12rpx;
    }
  }
  .pay_time {
    width: 100%;
    height: 58rpx;
    border-top: 1px solid rgb(238, 238, 238);
    border-bottom: 1px solid rgb(238, 238, 238);
    box-sizing: border-box;
    padding-left: 34rpx;
    line-height: 58rpx;
    font-family: PingFang-SC-Medium;
    color: rgb(166, 166, 166);
    font-size: 24rpx;
  }
}
</style>
 
