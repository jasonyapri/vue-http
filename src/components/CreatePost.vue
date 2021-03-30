<template>
    <div>
        <h2>Create Post</h2>
        <form @submit.prevent="createPost"> <!-- prevent modifier is used so that the page is not refreshed when the form is submitted -->
            <div>
                <label for="userId">User ID</label>
                <input type="text" id="userId" v-model="formData.userId">
            </div>
            <div>
                <label for="title">Post Title</label>
                <input type="text" id="title" v-model="formData.title">
            </div>
            <div>
                <label for="body">Post Body</label>
                <input type="text" id="body" v-model="formData.body">
            </div>
            <button>Create</button>
        </form>
    </div>
</template>

<script>
    import axios from 'axios'

    export default {
        name: 'CreatePost',
        data() {
            return {
                formData: {
                    userId: '',
                    title: '',
                    body: '',
                }
            }
        },
        methods: {
            createPost() {
                axios.post('http://jsonplaceholder.typicode.com/posts', this.formData)
                .then(response => console.log(response))
                .catch(error => console.log(error))
            }
        }
    }
</script>

<style scoped>

</style>