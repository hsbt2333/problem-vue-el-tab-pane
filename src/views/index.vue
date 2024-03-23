<template>
    <div style="width: 800px;margin: auto;margin-top: 100px;">
      <el-divider>my-tabs</el-divider>
      <my-tabs :list="list">
      </my-tabs>
      <el-divider>my-select</el-divider>
      <my-select :list="list"></my-select>
      <el-divider>el-tabs</el-divider>
      <el-tabs v-model="value" type="border-card" tab-position="left" style="height: 200px;">
          <el-tab-pane v-for="(item, index) in list" :key="index" :name="item.name" :label="item.label">
              {{ item.label }}
          </el-tab-pane>
      </el-tabs>
    </div>
</template>
<script>
import myTabs from '@/components/myTabs.vue'
import mySelect from '@/components/mySelect.vue';

export default {
  name: "index",
  components:{
    myTabs,
    mySelect
  },
  data() {
    return {
        value: '1',
        list: [
            {
                name: '1',
                label: '数据结构'
            },
            {
                name: '2',
                label: '操作系统'
            }
        ]
    }
  },
};
</script>
<style scoped>
</style>