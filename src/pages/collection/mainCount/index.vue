<template>
  <div  class="content" >
      
        <view class="logo">
          <img src="../../../../static/images/wechat.png" alt="">
        </view>
        <view class="number">185 6558 5286</view>

        <view class="btn set">
                设为主收款账号
        </view>

          <view class="btn unbind">
                解除绑定
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
.content{
  width: 100%;
  height: 1206rpx;
  background-color: #f4f4f4;
  box-sizing: border-box;
  padding-top: 86rpx;
  .logo{
    width: 100%;
    height: 120rpx;
    text-align: center;
    img{
        width: 120rpx;
        height: 120rpx;
    }
  }

  .number{
    width: 100%;
    text-align: center;
    font-family: PingFang-SC-Regular;
    color:#000;
    font-size: 36rpx;
    margin-top: 26rpx;
  }

  .btn{
    width: 690rpx;
    height: 88rpx;
    border-radius: 10rpx;
    margin-left: 27rpx;
    text-align: center;
    line-height: 88rpx;
    font-size: 36rpx;
    font-family: PingFang-SC-Medium;
  }
  .set{
    background-color: rgb(157,31,40);
    border: 1px solid rgb(157,31,40);
    color:#fff;
    margin-top: 107rpx;

  }
  .unbind{
    background-color: #fff;
    border: 1px solid rgb(157,31,40);;
    color:rgb(157,31,40);
    margin-top: 40rpx;
  }

}
</style>
 