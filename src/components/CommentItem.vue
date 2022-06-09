<template>
    <div class="comment">
        <div>    
            <div><b>Ism: </b>{{ comment.name }}</div>
            <div><b>Email: </b>{{ comment.email }}</div>
            <div><b>Post: </b> <i>"{{ comment.content }}"</i> </div>
        </div>
        <div>
            <my-btn class="btn btn-success" @click="$emit('remove', comment)">O'chirish</my-btn>
        </div>
    </div>
</template>
<script>
export default {
    name: 'my-button',
    props: {
            comment: {
                type: Object,
        }
    }    
}
</script>
<style scoped>
.comment{
    border: 3px solid #ccc;
    padding: 10px;
    margin-bottom: 10px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    background: rgba(0, 0, 0, 0.8);
    color: white;
    border-radius: 3vh;
}
@media (max-width: 700px) {
    .comment{
        padding: -10px;
        border-radius: 3vh;
    }
}
</style>
