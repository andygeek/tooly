<template>
  <div class="tooly-header__container">
    <NuxtLink to="/" class="tooly-title__text">
      <span class="tooly-t__text">T</span>
      <span class="tooly-ooly__text">ooly</span>
    </NuxtLink>
  </div>
</template>
<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: 'ToolyHeader',
})
</script>
<style scoped>
.tooly-header__container {
  margin: 10px;
}
.tooly-title__text {
  font-family: 'Roboto Slab', serif;
  display: flex;
  font-size: 40px;
  font-weight: 500;
  text-decoration: none;
  color: black;
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
</style>