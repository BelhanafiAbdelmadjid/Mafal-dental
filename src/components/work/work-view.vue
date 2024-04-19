<template>
    <desk v-if="widthLarge" ></desk>
    <mobile v-else ></mobile>

</template>
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
    }

}
</script>
<style>

</style>