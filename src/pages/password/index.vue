<template>
  <div  class="content" >
      
        <view class="text ">设置密码</view>
        <view class="phone_con">
            <input type="text" placeholder="仅数字，英文，长度在8~16字符之间" maxlength="16" v-model="pwd1"  @blur="velidCode">
        </view>
         <view class="warm mt35" v-show="isRight">仅数字，英文，长度在8~16字符之间</view>
     
       <view class="text mt35">再次输入密码</view>
         <view class="code_con">
            <view class="code">
              <input type="number" placeholder="请输入验证码" v-model="pwd2" @blur="isSame" >
            </view>
         </view>

      <view class="warm mt35" v-show="same">两次密码输入不一致</view>
       <view class="login_btn" @click="submit">确定</view>
  </div>
</template>

<script>
export default {
  data() {
    return {
      pwd1: "",
      pwd2: "",
      isRight: false, //密码规则是否正确
      same: false //两次输入是否相同
    };
  },

  components: {},

  computed: {},
  methods: {
    //校验密码
    velidCode() {
      var that = this;
      var reg = /^[A-Za-z0-9]{6,18}$/;
      if (!reg.test(that.pwd1)) {
        that.isRight = true;
      }else{
        that.isRight = false;

      }
    },

    // 验证两次输入是否相同
    isSame(){
      var that = this;
      if (that.pwd1 != that.pwd2) {
          that.same = true;
          return;
        }else{
          that.same = false;
        }
    },

    // 确定提交
    submit() {
      
      console.log("提交成功");
    }
  }
};
</script>

 <style lang="less" scoped>
.content {
  width: 100%;
  height: 1206rpx;
  box-sizing: border-box;
  padding-top: 300rpx;
  padding-left: 85rpx;
  padding-right: 85rpx;

  .text {
    font-family: PingFang-SC-Regular;
    color: rgb(51, 51, 51);
    font-size: 30rpx;
    margin-left: 35rpx;
  }
  .warm {
    font-family: PingFang-SC-Regular;
    color: rgb(255, 21, 21);
    font-size: 24rpx;
    margin-left: 35rpx;
  }
  .mt35 {
    margin-top: 35rpx;
  }
  .phone_con {
    width: 580rpx;
    height: 88rpx;
    border-radius: 44rpx;
    border: 1px solid rgb(191, 191, 191);
    margin-top: 20rpx;
    // box-shadow: 0 0 8rpx rgba(198,50,62,0.14);
    overflow: hidden;
    box-sizing: border-box;
    padding-left: 35rpx;
    .number {
      display: inline-block;
      height: 100%;
      line-height: 88rpx;
      float: left;
      font-family: PingFang-SC-Regular;
      font-size: 30rpx;
      color: rgb(51, 51, 51);
    }
    input {
      float: left;
      width: 100%;
      margin-top: 18rpx;
      font-size: 30rpx;
      color: #000;
    }
  }
  input::-webkit-input-placeholder,
  textarea::-webkit-input-placeholder {
    color: rgb(191, 191, 191);
    font-size: 30rpx;
  }
  input:-moz-placeholder,
  textarea:-moz-placeholder {
    color: rgb(191, 191, 191);
    font-size: 30rpx;
  }
  input::-moz-placeholder,
  textarea::-moz-placeholder {
    color: rgb(191, 191, 191);
    font-size: 30rpx;
  }
  input:-ms-input-placeholder,
  textarea:-ms-input-placeholder {
    color: rgb(191, 191, 191);
    font-size: 30rpx;
  }
  .code_con {
    width: 580rpx;
    height: 88rpx;
    border-radius: 44rpx;
    margin-top: 20rpx;
    clear: both;
    .code {
      width: 580rpx;
      height: 88rpx;
      float: left;
      border: 1px solid rgb(172, 172, 172);
      border-radius: 44rpx;
      input {
        width: 100%;
        height: 100%;
        line-height: 88rpx;
        border-radius: 44rpx;
        box-sizing: border-box;
        padding-left: 35rpx;
        font-size: 30rpx;
      }
    }
    .getCode {
      width: 225rpx;
      height: 88rpx;
      float: right;
      border: 1px solid rgba(198, 50, 62, 0.14);
      box-shadow: 0 0 8rpx rgba(198, 50, 62, 0.14);
      border-radius: 44rpx;
      line-height: 88rpx;
      font-size: 30rpx;
      color: rgb(167, 53, 61);
      font-family: PingFang-SC-Regular;
      text-align: center;
    }
  }

  .login_btn {
    width: 360rpx;
    height: 88rpx;
    text-align: center;
    line-height: 88rpx;
    background-color: rgba(169, 32, 43, 0.9);
    //  background:linear-gradient(to right, rgba(152,30,39,0.64), rgba(210,58,70,0.64),rgba(169,32,43,0.9));
    color: #fff;
    font-family: PingFang-SC-Medium;
    font-size: 36rpx;
    border-radius: 44rpx;
    margin-top: 67rpx;
    box-shadow: 1rpx 13rpx 29rpx rgba(201, 1, 1, 0.16);
    margin-left: 110rpx;
  }
}
</style>
 