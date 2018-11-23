<template>
  <div  class="content" >
       <!-- 搜索框 -->
      <div class="search">
        <div class="left">
            <input type="text" @focus="toHidden" @blur="toSearch" >
            <div class="txt" v-show="ishidden">
               <icon type="search" size="12" />
              <span class="tip">搜索流水号</span>
            </div>
        </div>
        <div class="right">
          <div class="line"></div>
          <div class="month_btn">
               <!-- 时间选择器 -->
            <view class="section">
              <picker mode="date" :value="date" start="2018-09" end="2020-09" fields="month" @change="bindDateChange">
                <view class="picker">
                月账单
                </view>
              </picker>
            </view>
          </div>
        </div>
      </div>
      <!-- 时间 -->
      <div class="date">{{date}}</div>
      <!-- 表单数据 -->
      <myTable :lists="lists"></myTable>


   
  </div>
</template>

<script>
// Use Vuex
import store from "./store";
import myTable from "@/components/Table";

export default {
  data() {
    return {
      ishidden: true, //是否隐藏
      lists: [
        {
          id: 1,
          order_id: "20181123001",
          type: 1,
          status: 0,
          total: "2200.00",
          server: "176.00",
          real_income: "1944.00",
          date: "2018-11-23 06:34"
        },
        {
          id: 2,
          order_id: "20181123003",
          type: 2,
          status: 1,
          total: "2500.00",
          server: "166.00",
          real_income: "2244.00",
          date: "2018-12-23 06:34"
        }
      ],
      date: "2018年09月"
    };
  },
  components: {
    myTable
  },

  computed: {},
  methods: {
    //隐藏文字
    toHidden() {
      var that = this;
      that.ishidden = false;
    },
    //搜索
    toSearch() {
      var that = this;
      that.ishidden = true;
    },
    bindDateChange: function(e) {
      var that = this;
      var str = e.mp.detail.value;
      var arr = str.split('-');
      that.date = arr[0] + '年' +arr[1] + '月';
      var tamp = new Date(str).getTime();
      console.log(tamp)
      
    }
  }
};
</script>

 <style lang="less" scoped>
.content {
  width: 100%;
  height: 1109rpx;
  background-color: #f4f4f4;
  box-sizing: border-box;
  .search {
    width: 100%;
    height: 88rpx;
    background-color: rgb(239, 239, 244);
    box-sizing: border-box;
    padding: 0rpx 24rpx 12rpx 15rpx;

    overflow: hidden;
    .left {
      width: 528rpx;
      height: 56rpx;
      background-color: #fff;
      float: left;
      border-radius: 28rpx;
      margin-top: 16rpx;
      position: relative;
      input {
        width: 100%;
        height: 100%;
        border-radius: 28rpx;
        padding-left: 40rpx;
      }
      .txt {
        position: absolute;
        left: 159rpx;
        top: 0;
        text-align: center;
        .tip {
          font-family: PingFang-SC-Regular;
          color: rgb(178, 178, 178);
          font-size: 26rpx;
          margin-left: 10rpx;
        }
      }
    }
    .right {
      float: right;
      width: 161rpx;

      margin-top: 11rpx;
      overflow: hidden;
      .line {
        width: 2rpx;
        height: 43rpx;
        background-color: rgb(181, 181, 181);
        float: left;
        margin-top: 12rpx;
      }
      .month_btn {
        width: 140rpx;
        height: 65rpx;
        float: right;
        color: rgb(125, 125, 125);
        border: 1px solid rgb(160, 160, 160);
        border-radius: 32rpx;
        font-family: PingFang-SC-Medium;
        font-size: 32rpx;
        text-align: center;
        line-height: 65rpx;
        position: relative;
        .section {
          width: 100%;
          position: absolute;
          left: 0;
          top: 0;
          text-align: center;
        }
      }
    }
  }
  .date {
    height: 85rpx;
    box-sizing: border-box;
    padding-top: 37rpx;
    padding-left: 32rpx;
    font-family: PingFang-SC-Bold;
    font-size: 28rpx;
    color: rgb(136, 136, 136);
  }
}
</style>
 