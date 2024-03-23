<template>
    <div>
        <el-tab-pane :name="name" :label="label">
            <slot></slot>
        </el-tab-pane>
        el-tab-pane div: {{ name }} - {{ label }}
    </div>
</template>

<script>
export default {
    name: 'myTabPane',
    props:{
        name: String,
        label: String
    }
}
</script>