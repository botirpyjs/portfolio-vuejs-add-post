<template>
    
    <div class="d-flex flex-column flex-md-row align-items-center pb-3 mb-4 border-bottom">
      <div class="d-flex align-items-center text-white text-decoration-none">
        <svg xmlns="http://www.w3.org/2000/svg" x="0px" y="0px" class="mt-2" width="50" height="50" viewBox="0 0 172 172" style=" fill:#000000;"><g fill="none" fill-rule="nonzero" stroke="none" stroke-width="1" stroke-linecap="butt" stroke-linejoin="miter" stroke-miterlimit="10" stroke-dasharray="" stroke-dashoffset="0" font-family="none" font-weight="none" font-size="none" text-anchor="none" style="mix-blend-mode: normal"><path d="M0,172v-172h172v172z" fill="none"></path><g fill="#2ecc71"><path d="M86,6.88c-43.63156,0 -79.12,35.48844 -79.12,79.12c0,43.63156 35.48844,79.12 79.12,79.12c43.63156,0 79.12,-35.48844 79.12,-79.12c0,-43.63156 -35.48844,-79.12 -79.12,-79.12zM64.8225,51.4925h26.445c12.55063,0 20.21,6.58438 20.21,16.985c0,7.095 -5.24062,13.4375 -11.825,14.62v0.7525c9.21813,1.075 15.265,7.51156 15.265,16.4475c0,11.94594 -8.68062,19.135 -23.1125,19.135h-26.9825zM74.0675,59.555v21.07h13.115c9.91688,0 15.05,-3.61469 15.05,-10.535c0,-6.67844 -4.82406,-10.535 -13.0075,-10.535zM74.0675,88.2575v23.1125h16.2325c9.93031,0 15.05,-3.99094 15.05,-11.61c0,-7.56531 -5.32125,-11.5025 -15.8025,-11.5025z"></path></g></g></svg>
        <span class="fs-4 pl-2"><b class="text-danger">Web frontend developer</b><br> Botir Akhmedov</span>
      </div>
<hr class="hr">
      <nav class="d-inline-flex mt-2 mt-md-0 ms-md-auto">
        <my-btn @click="showModal" class="px-2 py-2 text-decoration-none btn btn-primary mt-2">Yangi post qo'shish</my-btn>
      </nav>
    </div>    
    
</template>
<script> 
import MyBtn from './UI/MyBtn';
export default {
    props: {
        components:{
            MyBtn
        },
      showModal: {
        type: Function
      }
    }
    
}
</script>
<style scoped>
.hr{
  position: absolute;
  display: none;
}
@media (max-width: 700px) {
  .hr{
    height: 0px;
    width: 100%;
    border: 1px solid rgba(255, 255, 255, 0.7);
    background-color: transparent;
    position: relative;
    display: block;
  }
}
</style>