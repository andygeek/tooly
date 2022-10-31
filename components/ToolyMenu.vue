<template>
  <div class="tooly-menu__container">
    <el-tree
      :data="data"
      :default-expand-all="true">
        <template #default="{ node, data }">
          <span :class="{'node-title': !!data.isTitle}" class="custom-tree-node">
            <a class="menu-text__container" :href="`documentation/#${data.label.toLowerCase()}`">{{ node.label }}</a>
          </span>
        </template>
      </el-tree>
  </div>
</template>
<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
interface Tree {
  label: string
  children?: Tree[],
  isTitle?: boolean
}

@Component
export default class ToolyMenu extends Vue {

  data: Tree[] = [
    {
      label: 'List',
      isTitle: true,
      children: [
        {
          label: 'chunk',
        },
        {
          label: 'compact',
        },
        {
          label: 'concat',
        },
        {
          label: 'difference',
        },
        {
          label: 'drop',
        },
        {
          label: 'uniq',
        },
        {
          label: 'listToString',
        },
        {
          label: 'fill',
        },
        {
          label: 'flatten',
        },
        {
          label: 'findIndex',
        },
        {
          label: 'findLastIndex',
        },
        {
          label: 'indexOf',
        },
      ],
    }
  ]
}
</script>
<style scoped>
.tooly-menu__container {
  font-family: 'Source Sans Pro', sans-serif;
  font-size: 20px;
}
.menu-text__container {
  text-decoration: none;
  color: black;
}
</style>
<style>
.el-tree-node__content {
  height: 35px !important;
}
.node-title {
  font-weight: bold;
}
</style>