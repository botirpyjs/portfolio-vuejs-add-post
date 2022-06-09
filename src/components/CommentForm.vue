<template>
    <div>
        <div class="w-75 mx-auto">
            <h1 class="text-center text-secondary">Yangi post qo'shing!</h1>
            
            <form @submit.prevent>
                <my-input v-model="comment.name" placeholder="Ismingiz..." class="ss form-control" />
                <my-input v-model="comment.email" placeholder="Emailingiz..." class="ss form-control my-2" required />
                <my-input v-model="comment.content" placeholder="Postingiz..." class="ss form-control" />
                <div class="btn1 d-flex flex-row-reverse ">
                    <my-btn @click="createComment" class="btn btn-danger mt-3 w-25" >Qo'shish</my-btn>
                </div>
            </form>
        </div>        
    </div>
</template>
<script>
import MyBtn from './UI/MyBtn.vue';
export default {
  components: { 
      MyBtn 
    },
    data() {
        return {
            comment: {
                name: '',
                email: '',
                content: ''
            }
        }
    },
    methods: {
        createComment() {
            this.comment.id = Date.now();
            this.$emit('addComment', this.comment);
            this.comment = {
                name: "",
                email: "",
                content: "",
            }
        }
    },
}
</script>
<style scoped>
@media (max-width: 700px){
    button,
    input,
    h1{
        font-size: 15px;
    }
    .btn1{
        margin: 0;
        padding: 0;
        display: flex;
        margin-left: -150px;
        justify-content: center;
        width: 400px !important;
    }
    h4{
        font-size: 15px;
    }
}
</style>
