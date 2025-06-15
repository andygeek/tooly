<template>
  <div class="font-sans text-lg">
    <el-tree
      :data="data"
      :default-expand-all="true"
      @node-click="handleNodeClick"
    >
      <template #default="{ node, data }">
        <span :class="{ 'font-bold': !!data.isTitle }" class="custom-tree-node">
          <a
            :ref="data.label"
            :href="`documentation/#${data.label.toLowerCase()}`"
            class="no-underline text-black"
            >{{ node.label }}</a
          >
        </span>
      </template>
    </el-tree>
  </div>
</template>
<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'
interface Tree {
  label: string
  children?: Tree[]
  isTitle?: boolean
}

@Component
export default class ToolyMenu extends Vue {
  data: Tree[] = [
    {
      label: 'Installation',
      isTitle: true,
    },
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
    },
  ]

  handleNodeClick(value: any) {
    const name = value.label
    const htmlElement = this.$refs[name] as HTMLLinkElement
    htmlElement.click()
  }
}
</script>
<style>
.el-tree-node__content {
  height: 35px !important;
}
</style>
