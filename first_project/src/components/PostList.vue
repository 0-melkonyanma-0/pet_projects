<template>

        <div class="post" v-for="post in posts" v-bind:key="post.id">
            <div class="post__title"><strong>Title:</strong> {{ post.title }} </div>
            <div class="post__description"><strong>Description:</strong> {{ post.body }} </div>
        </div>
   
</template>

<script>
    export default{
        props:{
            posts:{
                type:Array,
                required:true
            }
        }
    }
</script>

<style scoped>
    
    .post{
        padding: 15px;
        border: 5px solid beige;
        margin-top:10px;
    }

</style>