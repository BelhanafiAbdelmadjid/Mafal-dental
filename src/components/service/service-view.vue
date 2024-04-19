<template>  
    <div id="services" class="service-holder">
        <h1>Nos services</h1>
        <div class="content">
            <service>
                <template #icon >
                    <img src="../../assets/images/dental-implant.png" alt="">
                </template>
                <template #TypeService>
                    Implants
                </template>
            </service>
            <service>
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
            <service>
                <template #icon >
                    <img src="../../assets/images/extraction.png" alt="">
                </template>
                <template #TypeService>
                    Extractions
                </template>
            </service>
            <service>
                <template #icon >
                    <img src="../../assets/images/dental-care.png" alt="">
                </template>
                <template #TypeService>
                    Céramique
                </template>
            </service>
            <service>
                <template #icon >
                    <img src="../../assets/images/dental-veneer.png" alt="">
                </template>
                <template #TypeService>
                    Facettes
                </template>
            </service>
            <service>
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
    color: var(--gray-text-color);
    font-size: 24px;
}
@media only screen and (max-width: 1000px) {
    .service-holder .content{
        padding: 50px ;
        grid-template-columns: 1fr;
    }

}
</style>