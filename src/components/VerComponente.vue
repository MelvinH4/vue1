<template>
    <div>
        <h1>{{MensajeNormal}}</h1>
        <h1>{{titulo}}</h1>-<h1>{{clase}}</h1>
    </div>
</template>

<script>
    export default {
        name: 'VerComponente',
        props:['MensajeNormal','titulo','clase']
    }
</script>

<style scoped>

</style>