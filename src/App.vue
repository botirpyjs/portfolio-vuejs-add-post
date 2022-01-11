<template>
<div class="body">
        <navbar class="d-flex justify-content-between container" :showModal="showModal" />
    <div>
        <modalka v-model:show="modalVisible">
        <comment-form @addComment="createComment" />
        </modalka>
        <comment-list v-bind:comments="comments" @remove="removeComment" />            
    </div>
</div>
</template>
<script>
import CommentForm from './components/CommentForm';
import CommentList from './components/CommentList';
import Navbar from '@/components/Navbar';

export default {
    components:{
        CommentForm,
        CommentList,
        Navbar,
    },

    data() {
        return {
            comments: [
                // {id: 1, name: "Botir Akhmedov", email: "botircoders@gmail.com", content: "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Aspernatur, voluptatum."},
                // {id: 2, name: "Aziza Haydarova", email: "haydarova@gmail.com", content: "Lorem ipsum dolor, consectetur adipisicing elit. Aspernatur, voluptatum."},
                // {id: 3, name: "Davron Kamolov", email: "khamolov@gmail.com", content: "Lorem ipsum dolor, sit amet adipisicing elit. Aspernatur, voluptatum."},
                // {id: 3, name: "Davron Kamolov", email: "khamolov@gmail.com", content: "Lorem ipsum dolor, sit amet adipisicing elit. Aspernatur, voluptatum."},
                // {id: 3, name: "Davron Kamolov", email: "khamolov@gmail.com", content: "Lorem ipsum dolor, sit amet adipisicing elit. Aspernatur, voluptatum."},
                // {id: 3, name: "Davron Kamolov", email: "khamolov@gmail.com", content: "Lorem ipsum dolor, sit amet adipisicing elit. Aspernatur, voluptatum."}
            ],
            modalVisible: false,
        }
    },
    methods: {
        createComment(comment) {
            this.comments.push(comment);
            this.modalVisible = false;
        },
        removeComment(comment){
            this.comments = this.comments.filter(c => c.id !== comment.id);
        },
        showModal(){
            this.modalVisible = true;
        }
    },
}
</script>
<style>
.comment{
    padding: 10px;
    margin: 10px;
    border: 3px solid #ccc;
}
body{
    background-image: url("img/1.jpg");
    width: 100%;
    height: 625px;
    background-size: cover;
    background-attachment: fixed;
}
@media (max-width: 700px) {
    body{
    background-image: url("img/2.jpg");
    height: auto;
    background-size: cover;
    background-attachment: fixed;
    }
}
</style>