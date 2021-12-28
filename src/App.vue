<template>
    <div class="body">
        <br>
            <!-- <h1 class="text-center text-warning">Add post</h1> -->
        <div class="w-75 llk">
            <form @submit.prevent>
                
                <input @input="name = $event.target.value" :value="name" type="text" placeholder="Enter your name..." class="form-control">
                <input @input="email = $event.target.value" :value="email" type="email" placeholder="Enter your email..." class="form-control my-2">
                <input @input="post = $event.target.value" :value="post" type="text" placeholder="Enter your post..." class="form-control ">
                <div class="d-flex flex-row-reverse">
                <button @click="createPost" class="btn btn-primary mt-2 w-25">Add post</button>
                </div>
            </form>
            <hr class="hrrr">
        </div>
        <div class="posts w-75" v-for="posts in comments" v-bind:key="posts">
            <div><b>Name:</b> {{ posts.name }}</div>
            <hr class="hrr">
            <div><b>Email:</b> {{ posts.email }}</div>
            <hr class="hrr">
            <div class="w-75"><b>Post:</b> <span class="postd fst-italic">"{{ posts.post }}"</span></div>
        </div>
    </div>
</template>
<script>
export default {
    data() {
        return {
            comments: [
                {id: 1, name: 'Botir Akhmedov', email: 'botircoders@gmail.com', post: "Assalomu alaykum hurmatli mehmon. Siz bu joyga o'z postlaringizni joylashingiz mumkin."}
            ],
            name: "",
            email: "",
            post: ""
            
            // count: 0,
        }
    },
        methods: {
            createPost(){
                const newpost = {
                    id: Date.now(),
                    name: this.name,
                    email: this.email,
                    post: this.post
                }
                this.comments.push(newpost)
            }
        },
}
</script>
<style>
button,
input{
    border-radius: 10px !important;
    border: 1px solid black !important;
}
body{
    background-image: url(dark.jpg);
    height: auto;
    width: 100%;
    background-attachment: fixed;
    background-size: cover;
    background-repeat: repeat;
}
.hrr{
    border: 1px dashed black;
    margin: 0;
    padding: 0px;
    background: transparent;
    margin-top: 7px;
    margin-bottom: 7px;
}
.body{
    display: flex;
    flex-direction: column;
    flex-wrap: nowrap;
    align-content: center;
    justify-content: center;
    align-items: center;
}
.posts{
    background-color: #fff;
    margin-bottom: 17px;
    border: 2px rgb(100, 100, 100);
    border-style: dotted;
    box-shadow: rgba(214, 214, 214, 0.452) 3px 3px 10px 2px;
    border-radius: 0px;
    border-top-left-radius: 0px;
    border-top-right-radius: 35px;
    border-bottom-left-radius: 35px;
    border-bottom-right-radius: 0px;
    /* margin-left: 20px; */
    /* width: 1003px; */
    padding: 15px;
}
.hrrr{
    border: 1px solid white;
    background: transparent;
}
</style>