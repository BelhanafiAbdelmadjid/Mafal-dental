<template>
    <desk id="work" class="work-left" v-if="widthLarge" ></desk>
    <mobile id="work" class="work-left" v-else ></mobile>

</template>
<script setup>
import ScrollReveal from 'scrollreveal';
</script>
<script>

import firstWork from "../../assets/images/first_work.jpg"
import secondWork from "../../assets/images/second_work.jpg"
import thirdWork from "../../assets/images/third_work.jpg"

import desk from "./work-desktop.vue"
import mobile from "./work-mobile.vue"

export default{
    data(){
        return{
            firstWork:firstWork,
            secondWork:secondWork,
            thirdWork:thirdWork,
            widthLarge : window.innerWidth >= 850 ? true : false,
        }
    },
    components : {
      desk,
      mobile
    },
    mounted(){
      window.addEventListener('resize', ()=>{
            this.widthLarge = window.innerWidth >= 850 ? true : false;
            
        });
        const sr = ScrollReveal();
        sr.reveal('.work-left', {
        duration: 1000,
        origin: 'bottom',
        distance: '150px',
        easing: 'ease-in-out',
        });
    }

}
</script>
<style>

</style>