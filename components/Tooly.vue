<template>
  <div class="tooly__container">
    <div class="tooly-title__container">
      <span class="tooly-title__text">
        <span class="tooly-t__text">T</span>
        <span class="tooly-ooly__text">ooly</span>
      </span>
      <span class="tooly-subtitle__text">
        Tooly is a library to handle lists in Dart in an easy and practical way.
      </span>
    </div>
    <div>
      <nuxt-link to="/documentation" class="button-documentation__container">
        <el-button type="primary">
            Documentation
        </el-button>
      </nuxt-link>
      <el-button type="primary" @click="redirect" plain>Dart</el-button>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'

@Component
export default class Tooly extends Vue {
  redirect() {
    window.location.href = "https://pub.dev/packages/tooly"
  }
}
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
  flex-direction: column;
  align-items: center;
  margin-inline: 15px
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
.button-documentation__container {
  margin-right: 10px;
}
</style>
