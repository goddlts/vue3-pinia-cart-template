<template>
  <div id="container">
    <div>
      <h3 class="title">Pinia - 购物车示例</h3>
      <div class="pop-cart">
        <PopCart  />
      </div>
    </div>
    <RouterView></RouterView>
  </div>
</template>

<script setup>
import PopCart from './components/PopCart.vue'
</script>

<style scoped>
#container {
  width: 980px;
  margin: 0 auto;
  padding: 10px;
}

.pop-cart {
  float: right;
}

.title {
  font-size: 20px;
  color: #333;
  margin-bottom: 20px;
}

.el-breadcrumb {
  padding: 20px 0;
}
</style>
