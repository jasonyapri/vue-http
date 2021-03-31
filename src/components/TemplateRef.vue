<template>
    <!-- Register a reference to an htlm component or a child component inside a parent's component -->
    <input type="text" ref="inputRef" />
    <PostList ref="postListRef"/>
</template>

<script>
    import PostList from './PostList.vue'

    export default {
        name: 'TemplateRef',
        components: {
            PostList
        },
        mounted() {
            console.log(this.$refs.postListRef)
            this.$refs.inputRef.focus()
        }
    }
</script>

<style scoped>

</style>