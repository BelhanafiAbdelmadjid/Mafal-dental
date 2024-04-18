<template>
    <largeLocation v-if="widthLarge" ></largeLocation>
    <largeMobile v-else ></largeMobile>
</template>
<script>
import largeLocation from "./location-view.vue"
import largeMobile from "./location-mobile.vue"
export default{
    data(){
        return{
            widthLarge : window.innerWidth >= 1000 ? true : false,
        }
    },
    components : {
        largeLocation,
        largeMobile
    },
    mounted(){
        window.addEventListener('resize', ()=>{
            this.widthLarge = window.innerWidth >= 1000 ? true : false;
        });
    },
}
</script>
<style>
</style>