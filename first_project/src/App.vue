<template>

    <div class="app">
       <post-form/>
       <post-list :posts="posts"/> <!-- HERE WE GIVE PROPS -->
    </div>
   
</template>

<script>
    import PostForm from "@/components/PostForm.vue";
    import PostList from "@/components/PostList.vue";
        
    export default{
        components:{
            PostForm,PostList
        },
        data(){
            return {
               posts:[
                {id:1,title:"Anime started1",body:"Discription1"},
                {id:2,title:"Anime started2",body:"Discription2"},
                {id:3,title:"Anime started3",body:"Discription3"},
                {id:4,title:"Anime started4",body:"Discription4"},
                {id:5,title:"Anime started5",body:"Discription4"},
               ],
               title:'',
               body: '',
            };
        },
        methods:{
            createPost(){
                const newPost = {
                    id:Date.now(),
                    title:this.title,
                    body:this.body,
                }

                this.posts.push(newPost);
                
                this.title = '',
                this.body = '';
            },
        }
    }
</script>

<style>
    *{
        margin:0;
        padding: 0;
        box-sizing: border-box;
    }

    .app{
        padding: 20px;
    }

</style>