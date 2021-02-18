<template>
  <div class="pad-15">
    <!-- 库存数据 -->
    <div class="flex flex-around pad-10 data-info-box border-radius-5">
      <div class="align-c">
        <span class="font-24 font-w">8888</span>
        <span class="mar-10 font-color-9">总库存</span>
      </div>
      <div class="align-c">
        <span class="font-24 font-w">100</span>
        <span class="mar-10 font-color-9">本月新入库</span>
      </div>
    </div>
    <!-- 库存管理 -->
    <div class="mar-t-15">
      <span class="font-w">
        库存管理
      </span>
      <div class="mar-t-15 flex flex-wrap pad-10 bg-color-white" style="box-shadow: 0rpx 4rpx 6rpx 4rpx #f2f2f2;">
        <div class="flex-col" @click="goAddGoods">
          <div class="btn-bg width-48 height-48 flex flex-center border-radius-5">
            <img class="width-26 height-26" src="../../img/warehousing.png" alt="">
          </div>
          <span class="font-12 mar-t-6 font-color-9">采购入库</span>
        </div>
        <div class="flex-col mar-l-20" @click="goOutStock">
          <div class="btn-bg width-48 height-48 flex flex-center border-radius-5">
            <img class="width-26 height-26" src="../../img/out-of-stock.png" alt="">
          </div>
          <span class="font-12 mar-t-6 font-color-9">商品出库</span>
        </div>
        <div class="flex-col mar-l-20">
          <div class="btn-bg width-48 height-48 flex flex-center border-radius-5">
            <img class="width-26 height-26" src="../../img/in-stock.png" alt="">
          </div>
          <span class="font-12 mar-t-6 font-color-9">库存信息</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
    }
  },
  methods: {
    goAddGoods () {
      wx.navigateTo({url: '/pages/warehousing/main'})
    },
    goOutStock () {
      wx.navigateTo({url: '/pages/outStock/main'})
    }
  }
}
</script>

<style lang="less" scoped>
.data-info-box {
  background: #fff;
  box-shadow: 0rpx 4rpx 6rpx 4rpx #f2f2f2;
}
.btn-bg {
  background: #f5f5f5;
}
</style>