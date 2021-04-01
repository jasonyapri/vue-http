<template>
    <h1>Reusability with Mixins</h1>
    <ClickCounter />
    <HoverCounter />
</template>

<script>
    import ClickCounter from './components/ClickCounter.vue'
    import HoverCounter from './components/HoverCounter.vue'

    export default {
        name: 'App',
        components: {
            ClickCounter,
            HoverCounter,
        }
    }
</script>

<style scoped>
    #app {
        font-family: Avenir, Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: center;
        color: #2c3e50;
        margin-top: 60px;
    }
</style>