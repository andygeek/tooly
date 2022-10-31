<template>
  <div class="tooly__container">
    <div class="tooly-title__container">
      <span class="tooly-title__text">Tooly</span>
      <span class="tooly-subtitle__text">
        Tooly is a package based in Lodash for Dart that contain utilities for working with lists, maps, sets and objects.
      </span>
    </div>
    <div>
      <el-button>Documentation</el-button>
      <el-button>Dart</el-button>
      <el-button>Ruby</el-button>
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
  font-size: 40px;
  font-weight: 500;
}
.tooly-subtitle__text {
  margin-block: 25px;
  text-align: center;
}
</style>
