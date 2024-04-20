<template>  
    <div id="services" class="service-holder">
        <div class="content">
            <h1 class="bottom-titel" >Nos services</h1>

            <service class="imp  bottom-scroll " >
                <template #icon >
                    <img src="../../assets/images/dental-implant.png" alt="">
                </template>
                <template #TypeService>
                    Implants
                </template>
            </service>

            <service class="pair bottom-scroll-quick" >
                <template #icon >
                    <!-- <svg width="36" height="36" viewBox="0 0 20 20" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path d="M5 0C2 0 0 3 0 6C0 8.11 1 11 2 12C3 13 4 20 6 20C10.54 20 8 13 10 13C12 13 9.46 20 14 20C16 20 17 13 18 12C19 11 20 8.11 20 6C20 3 18 0 15 0C12 0 12 1 10 1C8 1 8 0 5 0Z" fill="#222222"/>
                    </svg> -->
                    <img src="../../assets/images/tooth.png" alt="">

                </template>
                <template #TypeService>
                    Soins esthétique
                </template>
            </service>
            <service class="imp bottom-scroll" >
                <template #icon >
                    <img src="../../assets/images/extraction.png" alt="">
                </template>
                <template #TypeService>
                    Extractions
                </template>
            </service>
            <service class="pair bottom-scroll"  >
                <template #icon >
                    <img src="../../assets/images/dental-care.png" alt="">
                </template>
                <template #TypeService>
                    Céramique
                </template>
            </service>
            <service class="imp bottom-scroll-quick" >
                <template #icon >
                    <img src="../../assets/images/dental-veneer.png" alt="">
                </template>
                <template #TypeService>
                    Facettes
                </template>
            </service  >
            <service class="pair bottom-scroll" >
                <template #icon >
                    <img src="../../assets/images/x-ray.png" alt="">
                </template>
                <template #TypeService>
                    Radio
                </template>
            </service>
            
        </div>

    </div>
</template>
<script setup>
import ScrollReveal from 'scrollreveal';
</script>
<script>

import implant from "../../assets/images/implant.png"
import service from "./service-comp.vue"
export default{
    components : {
        service
    },
    data(){
        return{
            implant : implant
        }
    },
    mounted(){
        const sr3 = ScrollReveal();
        sr3.reveal('.bottom-titel', {
        duration: 1000,
        origin: 'top',
        distance: '150px',
        easing: 'ease-in-out',
        });
       if(window.innerWidth < 1000){
        const sr = ScrollReveal();
        sr.reveal('.imp', {
        duration: 1000,
        origin: 'left',
        distance: '150px',
        easing: 'ease-in-out',
        });
        
        const sr2 = ScrollReveal();
        sr2.reveal('.pair', {
        duration: 1000,
        origin: 'right',
        distance: '150px',
        easing: 'ease-in-out',
        });
       }else{
        const sr2 = ScrollReveal();
        sr2.reveal('.bottom-scroll', {
        duration: 1000,
        origin: 'bottom',
        distance: '150px',
        easing: 'ease-in-out',
        });
        const sr = ScrollReveal();
        sr.reveal('.bottom-scroll-quick', {
        duration: 750,
        origin: 'bottom',
        distance: '150px',
        easing: 'ease-in-out',
        });
       }
    }
}
</script>
<style scoped>
.holder-icon  img{
    width: 50px;
    height: 50px;
}
.service-holder-card .icon{


    width: auto;
    height: auto;

    background-size: cover;
    background-position: center center;
    background-repeat: no-repeat;
}
.service-holder{

    overflow: hidden;

    width: 100%;
    background-color: white;

    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;

    gap: 50px;
}

.service-holder .content{
    width: 100%;
    height: auto;
    background-color: var(--primary-color);

    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    grid-template-rows: auto;
    gap: 40px;

    padding: 50px 100px 50px 100px;
    box-sizing: border-box;

    -webkit-box-shadow:0px 0px 77px 5px rgba(62,66,66,0.27);
-moz-box-shadow: 0px 0px 77px 5px rgba(62,66,66,0.27);
box-shadow: 0px 0px 77px 5px rgba(62,66,66,0.27);
}
.service-holder h1{
    color: white;
    font-size: 24px;
    grid-column: 1/4;

    text-align: center
}
@media only screen and (max-width: 1000px) {
    .service-holder .content{
        padding: 50px ;
        grid-template-columns: 1fr;

        place-items: center;
    }
    .service-holder h1{
        grid-column: 1/2;
    }

}
</style>