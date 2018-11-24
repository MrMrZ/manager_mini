<template>
  <div  class="content" >
      
        <view class="logo">
          <img src="../../../../static/images/QRcode@2x.png" alt="">
        </view>



        <view class="tip">小提示：</view>

        
        <view class="steps">
           <ul>
             <li>1、点击下方的保存图片按钮</li>
             <li>2、打开微信扫一扫--从相册选取</li>
             <li>3、完成绑定</li>
           </ul>
        </view>

        <view class="tip mt30">当你想指定代理人收款时，只需要用代理人
的微信扫一扫此二维码即可。</view>

        <view class="btn " @click="saveImage">
                保存图片
        </view>

       
  </div>
</template>

<script>
export default {
  components: {},
  computed: {},
  methods: {
    // 保存到相册
    saveImage() {
      // 可以通过 wx.getSetting 先查询一下用户是否授权了 "scope.record" 这个 scope
      wx.getSetting({
        success(res) {
          if (!res.authSetting["scope.writePhotosAlbum"]) {
            wx.authorize({
              scope: "scope.writePhotosAlbum",
              success() {
                // 用户已经同意小程序使用录音功能，后续调用 wx.startRecord 接口不会弹窗询问
                wx.saveImageToPhotosAlbum({
                  filePath: "../../../../static/images/QRcode@2x.png",
                  success(res) {
                    alert("2222");
                  },
                  fail() {
                    console.log("失败了");
                  }
                });
              }
            });
          }
        }
      });
    }
  }
};
</script>

 <style lang="less" scoped>
.content {
  width: 100%;
  height: 1206rpx;
  background-color: #f4f4f4;
  box-sizing: border-box;
  padding-top: 110rpx;
  .logo {
    width: 100%;
    height: 380rpx;
    text-align: center;
    img {
      width: 380rpx;
      height: 380rpx;
    }
  }
  .tip {
    width: 100%;
    box-sizing: border-box;
    padding-left: 116rpx;
    padding-right: 103rpx;
    font-family: PingFang-SC-Bold;
    font-size: 28rpx;
    color: rgb(136, 136, 136);
    margin-top: 76rpx;
  }
  .mt30 {
    margin-top: 30rpx;
  }
  .steps {
    width: 100%;
    box-sizing: border-box;
    padding-left: 116rpx;
    margin-top: 36rpx;
    li {
      font-family: PingFang-SC-Medium;
      font-size: 34rpx;
      color: #000;
    }
  }
  .btn {
    width: 360rpx;
    height: 88rpx;
    border-radius: 10rpx;
    margin-left: 195rpx;
    text-align: center;
    line-height: 88rpx;
    font-size: 36rpx;
    font-family: PingFang-SC-Medium;
    background-color: rgb(11, 186, 7);
    color: #fff;
    margin-top: 119rpx;
  }
}
</style>
 