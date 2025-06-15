<template>
  <div class="m-2">
    <NuxtLink
      to="/"
      class="font-slab flex text-4xl font-medium no-underline text-black"
    >
      <span class="text-blue-600 cursor-pointer">T</span>
      <span>ooly</span>
    </NuxtLink>
  </div>
</template>
<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: 'ToolyHeader',
})
</script>
