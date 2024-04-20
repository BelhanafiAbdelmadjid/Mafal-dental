<template>
    <div class="location-main-holder" >
        <largeLocation v-if="widthLarge" ></largeLocation>
        <largeMobile v-else ></largeMobile>
    </div>
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
.location-main-holder{
    width: 100%;
}
</style>