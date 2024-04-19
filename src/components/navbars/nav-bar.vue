<template>
    <largeNav v-if="widthLarge" :hideNavScroll="hideNavScroll" >
        <template #links >
            <a href="#contact">Contact</a>
            <a href="#localisation">Localisation</a>
            <a href="#services">Services</a>
            <a href="#work">Notre travail</a>
        </template>
    </largeNav>
    <ThinNav v-else  :hideNavScroll="hideNavScroll" >
        <template #links >
            <a href="#contact">Contact</a>
            <a href="#localisation">Localisation</a>
            <a href="#services">Services</a>
            <a href="#work">Notre travail</a>

        </template>
    </ThinNav>
</template>
<script>
import largeNav from "./larg-nav.vue"
import ThinNav from "./thin-nav.vue"
export default{
    data(){
        return{
            widthLarge : window.innerWidth >= 650 ? true : false,
            old_y : 0,
            hideNavScroll : false,
        }
    },
    components : {
        largeNav,
        ThinNav
    },
    mounted(){
        window.addEventListener('resize', ()=>{
            this.widthLarge = window.innerWidth >= 650 ? true : false;
            
        });
        window.addEventListener('scroll', function() {
            var scrolled = window.scrollY;
            if(this.old_y < scrolled){
                console.log("down")
                this.hideNavScroll=true;
            }else{
                console.log("up")
                this.hideNavScroll=false;
            }
            this.old_y = scrolled;
            
            });
    },
    watch : {
        "window.scrollX"(){
            console.log("changed")
        }
    }
}
</script>
<style scoped>
nav .links a{
  text-decoration: none;
  color: rgb(69, 69, 69);
}
</style>