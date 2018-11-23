<template>
  <div  class="content" >
      
         <view class="title">
                  <view class="left">填写反馈</view>
          </view>

          <view class="_input">
            <view class="order_id">流水号：3124272564163</view>
            <textarea  :disabled="isWhite" class="feedback" maxlength="-1"  placeholder="请具体描述您遇到的问题，我们将尽快给您反馈。" v-model="desctiption" @input="calculate"></textarea>
            <span class="number">{{number}}<span class="all">/200</span> </span>
          </view>

        <view class="btn set">
                确定
        </view>

          <view class="btn unbind" @click="Call">
                拨打电话
        </view>
  </div>
</template>

<script>
export default {
  data(){
    return{
      desctiption:'',
      number:200,
      isWhite:false,
    }
  },
  components: {},
  computed: {},
  methods: {
    // 计算输入数字
    calculate(){
        var that = this;
        var len = that.desctiption.length;
        that.number = 200-len;
        if(that.number<=0){
           that.isWhite = true;
        }
    },
    // 拨打电话
    Call(){
      wx.makePhoneCall({
        phoneNumber: '18102840611' //仅为示例，并非真实的电话号码
      })
    }

  }
};
</script>

 <style lang="less" scoped>
.content{
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
      font-family: AdobeHeitiStd-Regular ;
      font-size: 28rpx;
      color:  rgb(136,136,136);
      box-sizing: border-box;
      padding-left: 32rpx;
    }
   }

._input{
  width: 700rpx;
  height: 400rpx;
  background-color: #fff;
  border-radius: 10rpx;
  margin-left: 25rpx;
  box-sizing: border-box;
  padding-left: 18rpx;
  padding-top: 30rpx;
  position: relative;
  .order_id{
    font-family: PingFang-SC-Medium;
    color:rgb(41,41,41);
    font-size: 30rpx;
  }
  .feedback{
    width: 670rpx;
    height: 310rpx;
    font-family: PingFang-SC-Regular;
    font-size: 24rpx;
    color:#000;
    box-sizing: border-box;
    padding-top: 50rpx;

  }
  .number{
    position: absolute;
    bottom: 18rpx;
    right: 21rpx;
    font-family: PingFang-SC-Medium;
    color:rgb(124,124,124);
    font-size: 30rpx;
     .all{
    font-family: PingFang-SC-Medium;
    font-size: 30rpx;
    color:rgb(41,41,41);
  }
  }
 
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
    margin-top: 100rpx;

  }
  .unbind{
    background-color: #fff;
    border: 1px solid rgb(157,31,40);;
    color:rgb(157,31,40);
    margin-top: 40rpx;
  }

}
</style>
 