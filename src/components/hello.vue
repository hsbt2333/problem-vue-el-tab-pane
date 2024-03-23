<template>
    <div>
        hello div: {{ name }} - {{ label }} <br />
        <slot></slot>
        
    </div>
</template>

<script>
export default {
    name: 'hello',
    props:{
        name: String,
        label: String
    }
}
</script>