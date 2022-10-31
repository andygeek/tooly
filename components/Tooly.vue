<template>
  <div class="tooly__container">
    <div class="tooly-title__container">
      <span class="tooly-title__text">
        <span class="tooly-t__text">T</span>
        <span class="tooly-ooly__text">ooly</span>
      </span>
      <span class="tooly-subtitle__text">
        Tooly is a multilanguage library to handle lists in Dart or arrays in Ruby in an easy and practical way.
      </span>
    </div>
    <div>
      <nuxt-link to="/documentation" class="button-documentation__container">
        <el-button type="primary">
            Documentation
        </el-button>
      </nuxt-link>
      <el-button type="primary" plain>Dart</el-button>
      <el-button type="danger" plain disabled>Ruby (soon...)</el-button>
      <el-button type="info" plain disabled>Go (soon...)</el-button>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: 'Tooly',
})
</script>
<style scoped>
.tooly__container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
.tooly-title__container {
  display: flex;
  width: 600px;
  flex-direction: column;
  align-items: center;
}
.tooly-title__text {
  font-family: 'Roboto Slab', serif;
  display: flex;
  font-size: 40px;
  font-weight: 500;
}
.tooly-subtitle__text {
  margin-block: 25px;
  font-size: 20px;
  text-align: center;
  font-family: 'Source Sans Pro', sans-serif;
}
.tooly-t__text {
  color: #0175c2;
  cursor: pointer;
}
.tooly-t__text:hover {
  color: red;
}
.button-documentation__container {
  margin-right: 10px;
}
</style>
