<template>
    <div id="contact" class="holder">
        <h1>À propos de nous</h1>
        <div class="content">
            <infoComp>
                <template #Icon>
                    <svg width="42" height="38" viewBox="0 0 20 16" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path
                            d="M18 0H2C0.9 0 0.00999999 0.9 0.00999999 2L0 14C0 15.1 0.9 16 2 16H18C19.1 16 20 15.1 20 14V2C20 0.9 19.1 0 18 0ZM18 4L10 9L2 4V2L10 7L18 2V4Z"
                            fill="#77BECA" />
                    </svg>

                </template>
                <template #Information>
                    <p class="information-titel" >Contactez-nous</p>
                    <p class="information-value" >(05) 58602778</p>
                    <p class="information-value" >mafal-cilnic@gmail.com</p>
                </template>
            </infoComp>
            <infoComp>
                <template #Icon>
                    <svg width="42" height="42" viewBox="0 0 32 32" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <g clip-path="url(#clip0_16_16)">
                            <path
                                d="M16 0C11.7565 0 7.68687 1.68571 4.68629 4.68629C1.68571 7.68687 0 11.7565 0 16C0 20.2435 1.68571 24.3131 4.68629 27.3137C7.68687 30.3143 11.7565 32 16 32C20.2435 32 24.3131 30.3143 27.3137 27.3137C30.3143 24.3131 32 20.2435 32 16C32 11.7565 30.3143 7.68687 27.3137 4.68629C24.3131 1.68571 20.2435 0 16 0ZM17.5 7.5V16C17.5 16.5 17.25 16.9688 16.8313 17.25L10.8312 21.25C10.1437 21.7125 9.2125 21.525 8.75 20.8312C8.2875 20.1375 8.475 19.2125 9.16875 18.75L14.5 15.2V7.5C14.5 6.66875 15.1687 6 16 6C16.8313 6 17.5 6.66875 17.5 7.5Z"
                                fill="#77BECA" />
                        </g>
                        <defs>
                            <clipPath id="clip0_16_16">
                                <rect width="32" height="32" fill="white" transform="matrix(-1 0 0 1 32 0)" />
                            </clipPath>
                        </defs>
                    </svg>
                </template>
                <template #Information>
    
                    <p class="information-titel" style="white-space: nowrap;" >Nous sommes ouvert le</p>
                    <p class="information-value-classic" >Dim - Jeu: 8:00 à 18h</p>
                    <p class="information-value-classic" >Samedi: 8:00 à 18h</p>
                </template>
            </infoComp>
        </div>
    </div>
</template>
<script>
import infoComp from "@/components/informations/info-comp.vue"
export default{
    components : {
        infoComp
    }
}
</script>
<style scoped>
.holder h1{
    color: var(--gray-text-color);
    font-size: 24px;
}
.content .information-titel{
    font-weight: 900;
    font-size: 22px;
    color: var(--gray-text-color);
    white-space: nowrap;

}
.content .information-value{
    font-weight: 500;
    font-size: 20px;
    white-space: nowrap;

}
.content .information-value-classic{
    font-weight: 500;
    font-size: 20px;
    white-space: nowrap;

}
.holder{
    width: 100%;
    height: auto;

    background-color: white;

    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;

    gap: 30px;

    padding-top: 20vh;
    padding-bottom: 20vh;
    padding-left: 10vw;
    padding-right: 10vw;
    box-sizing: border-box;
}
.holder .content{
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;

    background-color: var(--secondary-color);

    width: 100%;
    height: auto;

    gap: 2px;

    -webkit-box-shadow:0px 10px 121px 6px rgba(62,66,66,0.03);
-moz-box-shadow: 0px 10px 121px 6px rgba(62,66,66,0.03);
box-shadow: 0px 10px 121px 6px rgba(62,66,66,0.03);
}
.holder .info{
    width: 100%;
    height: 30vh;

    background-color: white;
    background-color: red;
}

@media only screen and (max-width: 1000px) {
    .holder .content {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }

    .content .information-titel {
        font-size: 18px;

    }

    .content .information-value {
        font-size: 16px;

    }

    .content .information-value-classic {
        font-size: 16px;

    }
    .holder{
        padding-top: 10vh;
        padding-bottom: 10vh;
    }

}
</style>