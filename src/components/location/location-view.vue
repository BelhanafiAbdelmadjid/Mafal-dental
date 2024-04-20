<template>
    <div id="localisation" class="holder-location">
        <div @click="openMaps()" class="map"></div>
        <div class="text-location">
            <div class="section">
                <h1>Où sommes-nous ?</h1>
                <p>
                    <span style="display: flex;align-items: center;gap: 5px;" >
                        <svg width="20" height="20" viewBox="0 0 44 44" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <path
                                d="M22 42C33.046 42 42 33.046 42 22C42 10.954 33.046 2 22 2C10.954 2 2 10.954 2 22C2 33.046 10.954 42 22 42Z"
                                stroke="#77BECA" stroke-width="4" />
                            <path
                                d="M2 18.84C5.015 17.417 7.245 17.218 8.69 18.245C10.857 19.785 11.128 26.064 16.058 23.064C20.987 20.063 13.947 18.84 15.475 14.494C17.003 10.147 22.008 13.524 22.505 8.763C22.837 5.589 19.041 4.37401 11.115 5.11901"
                                stroke="#77BECA" stroke-width="4" />
                            <path
                                d="M34 6C28.286 10.989 26.29 14.001 28.013 15.037C30.597 16.592 31.693 14.403 34.847 15.037C38 15.671 37.317 19.946 35.659 19.946C34 19.946 25.41 18.852 25.843 23.865C26.275 28.878 31.443 29.62 31.443 32.421C31.443 34.288 30.299 37.146 28.013 40.994M4.104 30.926C4.78567 30.6261 5.47105 30.3348 6.16 30.052C10.007 28.498 12.862 28.132 14.724 28.953C18.016 30.406 16.75 33.34 17.782 34.421C18.812 35.502 21.388 35.188 21.388 37.244C21.388 38.615 20.928 40.164 20.006 41.89"
                                stroke="#77BECA" stroke-width="4" stroke-linecap="round" />
                        </svg>
                        Alger, Reghaia
                    </span>
                    <span>
                        Localisation disponible sur Google Maps !
                        
                    </span>
                    <a style="color: var( --break-color);" target="_blank"
                            href="https://www.google.com/maps?q=P8RV+JM4+Mafal+Dental+Clinic+Dr.Oumahammed,+Réghaïa&ftid=0x128e43461208d9cd:0x8591642501344794&hl=fr-DZ&gl=dz&entry=gps&g_ep=CAISBjYuNTguMRgAINeCA0ICRFo%3D&g_st=iw">
                            cliquez ici pour y accéder
                    </a>

                </p>

            </div>
            <div class="section">
                <h1>Vous n'arrivez toujours pas à nous localiser ?</h1>
                <p>N'hésitez pas à nous appeler au <span style="color:var( --break-color);"><a href="tel:0585602778" style="text-decoration: none;color:var(--break-color)"  class="information-value" >0558602778</a></span></p>
            </div>
        </div>
    </div>
</template>
<script setup>
import ScrollReveal from 'scrollreveal';
</script>
<script>
export default{
    methods : {
        openMaps(){
            window.open('https://www.google.com/maps?q=P8RV+JM4+Mafal+Dental+Clinic+Dr.Oumahammed,+Réghaïa&ftid=0x128e43461208d9cd:0x8591642501344794&hl=fr-DZ&gl=dz&entry=gps&g_ep=CAISBjYuNTguMRgAINeCA0ICRFo%3D&g_st=iw', '_blank')
        }
    },
    mounted(){
        const sr = ScrollReveal();
        sr.reveal('.text-location', {
        duration: 1000,
        origin: 'right',
        distance: '150px',
        easing: 'ease-in-out',
        });
        const sr2 = ScrollReveal();
        sr2.reveal('.map', {
        duration: 1000,
        origin: 'left',
        distance: '150px',
        easing: 'ease-in-out',
        });
    }
}
</script>
<style scoped>
.holder-location{
    overflow: hidden;

    width: 100%;
    height: 70vh;
    min-height: 500px;


    display: flex;

    background-color: white;
}
.holder-location .map{
    width: 100%;
    height: 100%;

    background-image: url("../../assets/images/Mafal-location-map.png");
    background-size: cover; 
    background-position: center center; 
    background-repeat: no-repeat; 

    -webkit-box-shadow:0px 10px 144px 6px rgba(62,66,66,0.09);
-moz-box-shadow: 0px 10px 144px 6px rgba(62,66,66,0.09);
box-shadow: 0px 10px 144px 6px rgba(62,66,66,0.09);
}
.holder-location .text-location{
    width: 100%;

    padding-left: 20px;
    box-sizing: border-box;

    padding: 5px;
    box-sizing: border-box;

    background-color: var(--secondary-color);
}
.holder-location .text-location .section{
    color: var(--gray-text-color);

    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: flex-start;

    gap: 5px;

}
.holder-location .text-location .section p{
    font-weight: 500;

    padding: 20px;
    box-sizing: border-box;
    font-size: 18px;

    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: flex-start;

    gap: 5px;
}
@media only screen and (max-width: 1000px) {
    .holder-location{
        flex-direction: column-reverse;
        align-items: center;
        justify-content: center;

    }
    .holder-location .text-location{
        width: 100%;

        padding-left: 0px;
    }
    .holder-location .text-location .section{
    color: var(--gray-text-color);

    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;


    }
    .holder-location .text-location{
    padding-left: 0px;
    }
    .holder-location .text-location .section p{
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }
 
}
</style>
