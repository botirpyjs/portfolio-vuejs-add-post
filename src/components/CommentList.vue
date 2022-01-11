<template>
<div v-show="comments.length > 0">
    <h3 class="post text-center text-success">Tashlangan postlar</h3>

    <comment-item
    class="w-75 mx-auto comment"
    v-for="comment in comments"
    :comment="comment"
    :key="comment.id"
    @remove="$emit('remove', comment)"
    />
</div>
<div v-show="comments.length === 0">
    <h3 class="post text-center text-danger">Sizda tashlangan postlar yo'q</h3>
</div>
</template>
<script>
import CommentItem from './CommentItem';
export default {
    components: {
        CommentItem
    },
      props:{
        comments:{
            type: Array,
            required: true
        }
    }
}
</script>
<style scoped>
.post{
    background: rgba(0, 0, 0, 0.8);
    padding-top: 10px;
    padding-bottom: 10px;
}
</style>