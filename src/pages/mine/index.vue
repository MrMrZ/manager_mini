<template>
  <div class="content" >
       <div class="header ">
             <div class="left">
               <img src="../../../static/images/user@2x.png" alt="">
             </div>
             <div class="right">
                <div class="name">
                  大舜丽池 (汉正街一号)
                </div>
                <div class="phone">185 6558 5268</div>
             </div>
       </div>

       <div class="section">
         <ul>
           <li @click="toPages(1)">
             <div class="left">
               人员管理
             </div>
             <div class="right">
                <img src="../../../static/images/next@2x.png" alt="">
             </div>
           </li>
           <li @click="toPages(2)">
             <div class="left">
               收款账号
             </div>
             <div class="right">
                <img src="../../../static/images/next@2x.png" alt="">
             </div>
           </li>
           <li @click="toPages(3)">
             <div class="left">
               我的消息
             </div>
             <div class="right">
                <img src="../../../static/images/next@2x.png" alt="">
             </div>
           </li>
           <li class="mt30">
             <div class="left">
               到账提醒方式：短信
             </div>
             <div class="right">
                <switch checked bindchange="switch1Change" class="btn"/>
             </div>
           </li>
           <li class="mt30">
             <div class="left">
               联系我们
             </div>
             <div class="right">
             </div>
           </li>
           <li class="mt30" @click="toPages(4)">
             <div class="left">
               退出登录
             </div>
             <div class="right">
             </div>
           </li>
         
         </ul>
       </div>
  </div>
</template>

<script>
import { formatTime } from "@/utils/index";

export default {
  components: {},

  data() {
    return {};
  },
   methods:{
       //  跳转页面
       toPages(index){
           var url = '';
            switch(index){
              case 1: // 人员管理
                  url = '../manager/add/main';
                  break;
              case 2: //  收款账号
                  url = '../collection/add/main';
                  break;
              case 3: //我的消息
                  url = '../message/lists/main';
                  break;
              case 4:
                  url = '../login/main';
                  break;
              default:

            }
           wx.navigateTo({
            url:url
           })
       },


       toLogin(){
          wx.navigateTo({
            url:'../password/main'
           })
       }
   },

  created() {}
};
</script>

 <style lang="less" scoped>
.content {
  height: 1109rpx;
  background-color: #f4f4f4;
  box-sizing: border-box;
  padding-top: 30rpx;
  //  头部
  .header {
    width: 100%;
    height: 176rpx;
    background-color: #fff;
    box-sizing: border-box;
    padding-top: 23rpx;
    padding-left: 28rpx;
    overflow: hidden;

    .left {
      width: 130rpx;
      height: 130rpx;
      float: left;
      border-radius: 50%;
      img {
        width: 130rpx;
        height: 130rpx;
      }
    }
    .right {
      width: 60%;
      height: 100%;
      float: left;
      margin-left: 27rpx;
      box-sizing: border-box;
      padding-top: 16rpx;
      .name {
        font-size: 40rpx;
        font-family: PingFang-SC-Medium;
        color: #000;
      }
      .phone {
        font-size: 26rpx;
        font-family: PingFang-SC-Medium;
        color: rgb(124, 124, 124);
        margin-top: 12rpx;
      }
    }
  }
  //  中间内容
  .section {
    width: 100%;
    margin-top: 30rpx;
    border-top: 1rpx solid rgb(229, 229, 229);
    background-color: #f4f4f4;
    ul {
      .mt30 {
        margin-top: 30rpx;
      }
      li {
        width: 100%;
        height: 88rpx;
        overflow: hidden;
        box-sizing: border-box;
        padding-left: 30rpx;
        padding-right: 30rpx;
        background-color: #fff;
        .left {
          float: left;
          line-height: 88rpx;
          font-family: PingFang-SC-Medium;
          font-size: 34rpx;
          color: #000;
        }
        .right {
          float: right;
          line-height: 88rpx;
          img {
            width: 16rpx;
            height: 26rpx;
          }
          .btn {
            width: 104rpx;
            height: 74rpx;
          }
        }
      }
    }
  }
}
</style>
 