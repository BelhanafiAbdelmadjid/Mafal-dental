<template>
    <footer>
        <div class="slogan" >
            <img src="../../assets/images/mafal-logo.png" alt="">
            <p>Your smile our mission.</p>
        </div>
        <div class="Our-services" >
            <p class="underlined" >Navigation</p>
            <ul>
                <li><a href="#contact">Contact</a></li>
                <li><a href="#localisation">Localisation</a></li>
                <li><a href="#services">Services</a></li>
                <li><a href="#services">Notre travail</a></li>
            </ul>
        </div>
        <div class="contact-footer">
            <h3>Contactez-nous</h3>
            <div class="links-holder" >
                <p>
                    <a href="mailto:mafal-dental@gmail.com" class="information-value" >mafal-cilnic@gmail.com</a>
                </p>
                <p>
                    <a href="tel:0585602778" style="text-decoration: none;color:black"  class="information-value" >0558602778</a>
                </p>
                <p>
                    <a href="https://www.instagram.com/mafal_dentalclinic/" target="_blank" >Instagram</a>
                </p>
            </div>
        </div>
    </footer>
</template>

<script>
export default{

}
</script>
<style scoped>
footer .underlined{
    position: relative;
}
footer .underlined::after{
    content: "";
    width: 40%;
    bottom: -2px;
    left: 0;
    height: 2px;
    position: absolute;
    background-color: var(--details-color);
}

footer .Our-services{

    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: flex-start;

    box-sizing: border-box;

    color: white;

    gap: 10px;
}
footer .Our-services ul li{
    list-style: none;
    padding-left:15px ;
    font-size: 18px;
}
footer .Our-services p{
    font-weight: 900;
    font-size: 20px;
}
footer{


    position: relative;
    height: 40vh;
    min-height: 200px;
    width: 100%;

    background-image: url("../../assets/images/footer.jpg");
    background-size: cover;
    background-position: center center;
    background-repeat: no-repeat;

    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;

    padding-left: 50px;
    padding-right: 50px;

    box-sizing: border-box;
}

footer::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: -0;
  background-color: var(--primary-color); /* Replace with your primary color */
  filter: brightness(110%);
  opacity: 0.65; /* Adjust the filter effect as needed */
}

footer .slogan{
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: center;

    color: white;
    font-size: 20px;
}
footer div{
    z-index: 99;
    width: 100%;
}
footer a{
    text-decoration: none;
    color: white;
}
footer .contact-footer{
    background-color: var(--secondary-color);

    height: 80%;
    width: auto;

    place-self: flex-end;

    border-top-left-radius: 20px;
    border-top-right-radius: 20px;

    -webkit-box-shadow:0px 0px 77px 5px rgba(255,255,255,0.22);
    -moz-box-shadow: 0px 0px 77px 5px rgba(255,255,255,0.22);
    box-shadow: 0px 0px 77px 5px rgba(255,255,255,0.22);

    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: center;

    gap: 16px;

    padding: 20px;
    
    box-sizing: border-box;
}
footer .contact-footer h3{
    text-align: left;
    width: 100%;
    white-space: nowrap;
}
footer .contact-footer p{
    white-space: nowrap;
}
footer .contact-footer a{
    color: black;
}
footer .links-holder {
    text-align: left;
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: flex-start;
    gap: 5px;
}
@media only screen and (max-width: 800px) {
    footer{
        background-image: url("../../assets/images/footer.jpg");
        background-size: cover;
        background-position: center center;
        background-repeat: no-repeat;

        display: flex;
        flex-direction: column;
        justify-content: flex-start;
        align-items: center;

        height: auto;

        gap: 50px;

        padding-top: 40px;
        box-sizing: border-box;
    }
    footer .Our-services{
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;

        box-sizing: border-box;

        color: white;

        gap: 10px;
    }
    footer .contact-footer{
        background-color: var(--secondary-color);

        height: 80%;
        width: auto;

        place-self: center;

        border-top-left-radius: 20px;
        border-top-right-radius: 20px;

        -webkit-box-shadow:0px 0px 77px 5px rgba(255,255,255,0.22);
        -moz-box-shadow: 0px 0px 77px 5px rgba(255,255,255,0.22);
        box-shadow: 0px 0px 77px 5px rgba(255,255,255,0.22);

        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;

        padding: 20px;
        box-sizing: border-box;
    }
  
    }
</style>