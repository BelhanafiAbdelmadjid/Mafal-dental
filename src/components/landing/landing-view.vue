<template>
    <div class="landing-page">
        <div class="content landing-content ">
            <profComp></profComp>
            <div>
                <h1>CLINIQUE RENOMMÉE <br> SOURIRE ÉTOILÉ </h1>
                <p class="description">
                    Nous nous engageons à fournir des soins complets et personnalisés pour vous aider à atteindre et à
                    maintenir une santé bucco-dentaire optimale pour une vie pleine de <span style="white-space: nowrap;">sourires !</span>
                </p>
            </div>

            <a class="contact-button" href="#services">NOS SERVICES</a>
        </div>
    </div>
</template>
<script setup>
import ScrollReveal from 'scrollreveal';
</script>

<script>
import profComp from "./prof-comp.vue"

export default {
    components: {
        profComp
    },
    mounted(){
        const sr = ScrollReveal();
        sr.reveal('.landing-content', {
        duration: 1000,
        origin: 'left',
        distance: '150px',
        easing: 'ease-in-out',
        });
    }
}
</script>
<style scoped>
.landing-page {
    color: white;

    padding-top: var(--navbar-height);

    height: 100Vh;
    width: 100%;
    min-height: 480px;

    background-image: url('../../assets/images/landing-page-background.jpg');
    background-size: cover;
    background-position: center center;
    background-repeat: no-repeat;
    background-color: #f0f0f0;

    display: flex;
    align-items: center;
    justify-content: center;

    padding: 0px 50px 0px 50px;
    box-sizing: border-box;

}

.landing-page h1 {
    font-weight: 900;
    text-decoration: solid;
    font-size: 50px;

    white-space: nowrap;
}

.landing-page .content {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: center;

    gap: 10px;

}

.landing-page .description {
    margin-top: 10px;
    margin-bottom: 10px;

    font-family: 200;
    width: 50%;
    font-size: 14px;


    color: var(--break-color);
    font-weight: 500;
}

.landing-page .profession {
    margin-bottom: 10px;
}

.landing-page .contact-button {
    background-color: var(--primary-color);

    padding: 10px;

    border-radius: 5px;
    text-decoration: none;
    color: white;

    font-size: 16px;
    font-weight: 600;
}

@media only screen and (max-width: 600px) {
    .landing-page .description {
    width: 100%;

    }
    .landing-page h1 {
        font-size: 30px;
    }
    .landing-page .content {
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        justify-content: space-evenly;

        height: 40%;
        gap: 10px;

    }
}
</style>