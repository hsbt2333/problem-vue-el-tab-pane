<template>
    <el-tabs type="border-card" tab-position="left" style="height: 200px;">

        <my-tab-pane v-for="(item, index) in list" :key="item.name+index" :name="item.name" :label="item.label">

        </my-tab-pane>
        <hello v-for="(item, index) in list" :key="item.name+index+index" :name="item.name" :label="item.label">

        </hello>
        <slot></slot>
    </el-tabs>
</template>
<script>
import myTabPane from '@/components/myTabPane.vue'
import hello from '@/components/hello.vue'

export default {
    components:{
        myTabPane,
        hello
    },
    props:{
        list:[]
    },
    mounted() {
        console.log("mounted list:",this.list);
    },
}
</script>