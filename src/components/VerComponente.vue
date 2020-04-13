<template>
    <div>
        <p>{{title}}  {{nombre}}  {{apellido}}</p>
    </div>
</template>

<script>
    export default {
        name: 'VerComponente',
        props:['title','nombre','apellido']
    }
</script>

<style scoped>

</style>