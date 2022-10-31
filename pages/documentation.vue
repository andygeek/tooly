<template>
  <div class="documentation__container">
    <el-container>
      <el-header height="80px">
        <tooly-header></tooly-header>
      </el-header>
      <el-container>
        <el-aside width="300px">
          <tooly-menu></tooly-menu>
        </el-aside>
        <el-main style="height:calc(100vh - 80px)">
          <nuxt-content :document="page" />
        </el-main>
      </el-container>
    </el-container>
  </div>
</template>

<script>
import ToolyHeader from '~/components/ToolyHeader.vue';
import ToolyMenu from '~/components/ToolyMenu.vue';

export default {
  components: { ToolyHeader, ToolyMenu },
  async asyncData ({ $content }) {
    const page = await $content('hello').fetch()
    return {
      page
    }
  }
}
</script>
<style>
.documentation__container {
  height: 100vh;
  width: 100vw;
}
</style>
