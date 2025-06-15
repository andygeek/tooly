<template>
  <div class="flex flex-col items-center justify-center text-center">
    <div class="flex flex-col items-center mx-4">
      <span class="font-slab flex text-5xl font-medium">
        <span class="text-blue-600 cursor-pointer">T</span>
        <span>ooly</span>
      </span>
      <span class="my-6 text-xl font-sans">
        Tooly is a library to handle lists in Dart in an easy and practical way.
      </span>
    </div>
    <div class="flex gap-3">
      <nuxt-link to="/documentation">
        <el-button type="primary">Documentation</el-button>
      </nuxt-link>
      <el-button type="primary" plain @click="redirect">Dart</el-button>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'

@Component
export default class Tooly extends Vue {
  redirect() {
    window.location.href = 'https://pub.dev/packages/tooly'
  }
}
</script>
