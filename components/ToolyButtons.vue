<template>
  <div class="flex gap-4">
    <a
      href="https://pub.dev/packages/tooly"
      target="_blank"
      class="flex flex-col justify-end font-bold font-sans no-underline text-black"
    >
      <img src="~/assets/images/dart.png" class="h-12 w-12" />
      <span>pub.dev</span>
    </a>
    <a
      href="https://github.com/andygeek/tooly-dart"
      target="_blank"
      class="flex flex-col justify-end font-bold font-sans no-underline text-black"
    >
      <img src="~/assets/images/github.png" class="h-10 w-10 mb-1" />
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
