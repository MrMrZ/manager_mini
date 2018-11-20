<template>
  <div  class="content" >
       <!-- 搜索框 -->
      <div class="search">
        <div class="left">
            <input type="text">
            <div class="txt">
               <icon type="search" size="12" />
              <span class="tip">搜索流水号</span>
            </div>
        </div>
        <div class="right">
          <div class="line"></div>
          <div class="month_btn">月账单</div>
        </div>
      </div>
      <!-- 时间 -->
      <div class="date">2018年11月</div>
      <!-- 表单数据 -->
      <myTable></myTable>
  </div>
</template>

<script>
// Use Vuex
import store from './store'
import myTable from '@/components/Table'


export default {
  
  components: {
    myTable
  },

  computed: {
    
  },
  methods: {
     
  }
}
</script>

 <style lang="less" scoped>
  .content{
    width: 100%;
    height: 1109rpx;
    background-color: #f4f4f4;
    box-sizing: border-box;
    .search{
      width: 100%;
      height: 88rpx;
      background-color: rgb(239,239,244);
      box-sizing: border-box;
     padding: 0rpx 24rpx 12rpx 15rpx;
    
     overflow: hidden;
     .left{
       width: 528rpx;
       height: 56rpx;
       background-color: #fff;
       float: left;
       border-radius: 28rpx;
       margin-top: 16rpx;
       position: relative;
       input{
         width: 100%;
         height: 100%;
             border-radius: 28rpx;
       }
       .txt{
         position: absolute;
         left: 159rpx;
         top: 0;
         text-align: center;
         .tip{
           font-family: PingFang-SC-Regular;
           color:rgb(178,178,178);
           font-size: 26rpx;
           margin-left: 10rpx;
         }
       }

     }
     .right{
       float:right;
       width: 161rpx;

       margin-top: 11rpx;
       overflow: hidden;
       .line{
         width: 2rpx;
         height: 43rpx;
         background-color: rgb(181,181,181);
         float: left;
         margin-top: 12rpx;
       }
       .month_btn{
          width: 140rpx;
          height: 65rpx;
          float: right;
          color:rgb(125,125,125);
          border: 1px solid rgb(160,160,160);
          border-radius: 32rpx;
          font-family: PingFang-SC-Medium;
          font-size: 32rpx;
          text-align: center;
          line-height: 65rpx;
        

       }
     }
    }
    .date{
      height: 85rpx;
      box-sizing: border-box;
      padding-top:37rpx ;
      padding-left: 32rpx;
        font-family: PingFang-SC-Bold;
        font-size: 28rpx;
        color:rgb(136,136,136);
    }
  }

 </style>
 