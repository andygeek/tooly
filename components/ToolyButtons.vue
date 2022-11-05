<template>
  <div class="tooly-buttons__container">
    <a class="tooly-button--dart__container" href="https://pub.dev/packages/tooly" target="_blank">
      <img src="~/assets/images/dart.png" />
      <span>pub.dev</span>
    </a>
    <a class="tooly-button--github__container" href="https://github.com/andygeek/tooly-dart" target="_blank">
      <img src="~/assets/images/github.png" />
      <span>github</span>
    </a>
  </div>
</template>
<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: 'ToolyButtons',
})
</script>
<style scoped>
.tooly-buttons__container {
  display: flex;
  gap: 15px;
}
.tooly-button--dart__container {
  font-family: 'Source Sans Pro', sans-serif;
  font-weight: bold;
  flex-direction: column;
  display: flex;
  justify-content: flex-end;
  text-decoration: none;
  color: black;
}
.tooly-button--github__container {
  font-family: 'Source Sans Pro', sans-serif;
  font-weight: bold;
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
  text-decoration: none;
  color: black;
}
.tooly-button--dart__container img {
  height: 50px;
  width: 50px;
}
.tooly-button--github__container img {
  height: 40px;
  width: 40px;
  margin-bottom: 5px;
}
</style>