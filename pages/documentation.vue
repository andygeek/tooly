<template>
  <div class="documentation__container">
    <el-container>
      <el-header height="80px">
        <tooly-header></tooly-header>
      </el-header>
      <el-container>
        <el-aside width="250px" class="documentation-aside__container">
          <tooly-menu></tooly-menu>
        </el-aside>
        <el-main style="height:calc(100vh - 80px)" class="documentation-main__container">
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
    const page = await $content('documentation').fetch()
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
.documentation-main__container {
  font-family: 'Source Sans Pro', sans-serif;
  font-size: 18px;
}
.documentation-main__container h1 {
  font-weight: 600;
}
@media (max-width: 600px) {
  .documentation-aside__container {
    display: none;
  }
}
</style>
