<template>
    <footer>
        <div class="slogan" >
            <img src="../../assets/images/mafal-logo.png" alt="">
            <p>Your smile our mission.</p>
        </div>
        <div class="Our-services" >
            <p>Navigation</p>
            <ul>
                <li><a href="#contact">Contact</a></li>
                <li><a href="#localisation">Localisation</a></li>
                <li><a href="#services">Services</a></li>
            </ul>
        </div>
        <div class="contact-footer">
            <div style="text-align: left;width: 50%;" >
                <h3>Contactez-nous</h3>
                <p>
                   

                    <span  >mafal-cilnic@gmail.com</span>
                </p>
                <p>0558602778</p>
                <p>Instagram</p>
            </div>
        </div>
    </footer>
</template>

<script>
export default{

}
</script>
<style scoped>
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
  opacity: 0.85; /* Adjust the filter effect as needed */
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
    width: 80%;

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

    padding: 20px;
    
    box-sizing: border-box;
}
@media only screen and (max-width: 1000px) {
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
        width: 100%;

        place-self: none;

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