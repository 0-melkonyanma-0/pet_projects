<template>

        <form class="add-post" @submit.prevent>
            <h4>
                Create posts
            </h4>

            <input 
                v-bind:value='post.title' 
                @input="post.title = $event.target.value"  
                class="input"
                type="text" 
                placeholder="Title"
            >

            <input 
                v-bind:value='post.body'
                @input="post.body = $event.target.value"  
                class="input" 
                type="text" 
                placeholder="Description"
            >

            <input 
                class="btn-add-item" 
                type="submit" 
                value="create"
            >

        </form>
        
</template>

<script>
    export default{
        data(){
            return {
                post:{
                    title: '',
                    body: '',
                }
            }
        }
    }
</script>

<style scoped>

    form{
        display: flex;
        flex-direction: column;
    }

    .btn-add-item{
        margin-top: 10px;
        align-self: flex-end;
        padding: 10px;
        color:white;
        border: 1px solid blue;
        background-color: blue;
        border-radius: 10px;
    }

    .input{
        width: 100%;
        border: 5px solid beige;
        padding:10px 15px;
        margin-top: 10px;
    }

</style>