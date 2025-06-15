<template>
  <div class="min-h-screen w-screen flex flex-col">
    <header class="flex justify-between p-3">
      <tooly-header></tooly-header>
      <tooly-buttons></tooly-buttons>
    </header>
    <div class="flex flex-1">
      <aside class="hidden md:block w-64 p-4">
        <tooly-menu></tooly-menu>
      </aside>
      <main class="flex-1 overflow-y-auto p-4 prose font-sans">
        <nuxt-content :document="page" />
      </main>
    </div>
  </div>
</template>

<script>
import ToolyHeader from '~/components/ToolyHeader.vue'
import ToolyMenu from '~/components/ToolyMenu.vue'

export default {
  components: { ToolyHeader, ToolyMenu },
  async asyncData({ $content }) {
    const page = await $content('documentation').fetch()
    return {
      page,
    }
  },
}
</script>
