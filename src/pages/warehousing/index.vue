<template>
  <div class="pad-t-15">
    <div class="panel panel-box">
      <div class="flex v-align-c div-input mar-r-20">
        <div class="mar-r-10 width-80 font-color-3 font-15">商品名称</div>
        <div class="flex-item"><input  class="font-black" placeholder="请输入商品名称"/></div>
      </div>
      <div class="flex v-align-c div-input mar-r-20" @click="getGoodsCodeInfo">
        <div class="mar-r-10 width-80 font-color-3 font-15">商品编码</div>
        <div class="flex-item"><input class="font-black" v-model="goodsCode" placeholder="请输入商品编码"/></div>
      </div>
      <div class="flex v-align-c div-input mar-r-20">
        <div class="mar-r-10 width-80 font-color-3 font-15">商品数量</div>
        <div class="flex-item pad-t-4 pad-b-4">
          <van-stepper value="1" input-width="40px" button-size="32px" />
        </div>
      </div>
      <div class="flex v-align-c div-input mar-r-20">
        <div class="mar-r-10 width-80 font-color-3 font-15">商品单价</div>
        <div class="flex-item"><input class="font-black" placeholder="请输入商品单价"/></div>
        <span>元</span>
      </div>
    </div>
    <div class="mar-15 pad-t-10">
      <button size="default" class="primary-button font-w">添加入库</button>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      goodsCode: ''
    }
  },
  methods: {
    getGoodsCodeInfo () {
      let that = this
      wx.scanCode({
        success (res) {
          that.goodsCode = res.result
        },
        fail (error) {
          console.log(error)
        }
      })
    }
  }
}
</script>

<style lang="less" scoped>
  .div-input {
    border-bottom: 0.5px solid #ebebeb;
    margin-left: 20px;
    padding-top: 11px;
    padding-bottom: 11px;
    font-size: 13px;
  }
  .div-input:last-child {
    border-bottom: 0;
  }
  .primary-button{
    border-radius: 100px;
    background: #7427FF;
    color: #fff;
  }
</style>