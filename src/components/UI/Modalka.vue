<template>
    <div class="modal" v-if="show" @click.stop="hideModal">
        <div @click.stop class="modal_content">
            <slot></slot>
        </div>
    </div>
</template>
<script>
export default {
    name: 'modalka',
    props: {
        show: {
            type: Boolean,
            default: false
        },
    },
    methods: {
        hideModal(){
            this.$emit('update:show', false);
        }
    },
}
</script>
<style scoped>
.modal{
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, 0.7);
    z-index: 10;
    display: flex;
}
.modal_content{
    margin: auto;
    background: #fff;
    border-radius: 15px;
    padding: 20px;
    width: 50%;
    min-height: 100px;
}
@media (max-width: 700px){
    .modal_content{
        padding: 15px;
        width: 80%;
    }
}
</style>