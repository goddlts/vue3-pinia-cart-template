<template>
  <el-popover
    width="350"
    trigger="hover"
  >
    <el-table :data="cartProducts" size="small">
      <el-table-column property="title" width="130" label="商品"></el-table-column>
      <el-table-column property="price" label="价格"></el-table-column>
      <el-table-column property="count" width="50" label="数量"></el-table-column>
      <el-table-column label="操作">
        <template #default>
          <el-button size="small">删除</el-button>
        </template>
      </el-table-column>
    </el-table>
    <div>
      <p>共 0 件商品 共计¥0</p>
      <el-button size="small" type="danger" @click="router.push({ name: 'Cart' })">去购物车</el-button>
    </div>
    <template #reference>
      <el-badge :value="5" class="item" >
        <el-button type="primary">我的购物车</el-button>
      </el-badge>
    </template>
  </el-popover>
</template>

<script setup>
import { useRouter } from 'vue-router'

const router = useRouter()

const cartProducts = [
    { id: 1, title: 'iPad Pro', price: 500.01, isChecked: false, count: 0 },
    { id: 2, title: 'H&M T-Shirt White', price: 10.99, isChecked: false, count: 0 },
    { id: 3, title: 'Charli XCX - Sucker CD', price: 19.99, isChecked: false, count: 0 }
  ]
</script>

<style>

</style>
