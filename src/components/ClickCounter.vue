<template>
    <div>
        <button @click="incrementCount">Clicked {{ count }} times</button>
    </div>
</template>

<script>
    import CounterMixin from '../mixins/counter'

    export default {
        name: 'ClickCounter',
        data() {
            return{
                count: 100,
            }
        },
        mixins: [CounterMixin]
    }
    // It is possible to mixins computed properties, watchers and even lifecycle hooks
    // If the same variable is present in mixins and the vue file, then the one on the vue file will be used
</script>

<style scoped>

</style>