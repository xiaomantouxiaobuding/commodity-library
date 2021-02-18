<template>
  <div>
    <div>
      <van-cell-group>
        <van-field :value="text" label="出库商品" placeholder="请输入出库商品名称或商品编码" input-align="right"/>
      </van-cell-group>
    </div>
    <div>
      
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      text: ''
    }
  }
}
</script>

<style lang="less" scoped>

</style>