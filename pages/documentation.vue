<template>
  <div class="documentation__container">
    <el-container>
      <el-header>
        sdsdsds
      </el-header>
      <el-container>
        <el-aside width="300px">
          <a href="#fill">aaa</a>
        </el-aside>
        <el-main>
          <nuxt-content :document="page" />
        </el-main>
      </el-container>
    </el-container>
  </div>
</template>

<script>
export default {
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
