<template>
    <nav  >
        <div class="logo-holder">
            <img src="../../assets/images/mafal-logo.png" alt="">
        </div>
        <svg @click="openNav = true" width="18" height="12" viewBox="0 0 18 12" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M0 12V10H18V12H0ZM0 7V5H18V7H0ZM0 2V0H18V2H0Z" fill="#77BECA" />
        </svg>
        <div class="sidebar links" :class="{'sidebar-open' : openNav}">
            <div class="icon-close-holder">
              
                <svg @click="openNav = false" width="14" height="14" viewBox="0 0 14 14" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path d="M1.4 14L0 12.6L5.6 7L0 1.4L1.4 0L7 5.6L12.6 0L14 1.4L8.4 7L14 12.6L12.6 14L7 8.4L1.4 14Z" fill="#77BECA"/>
                </svg>

            </div>

            <div class="extra-links" @click="openNav=false" >
                <slot  name="links" ></slot>
            </div>
          
            
        </div>
    </nav>
</template>
<script>
export default{
    data(){
        return{
            openNav : false,
        }
    },
    props : ["hideNavScroll"]
}
</script>

<style scoped>
.hide-nav{
    background-color: red;
    left: -100%;
}

nav {
    position: sticky;
    left: 0;
    top: 0;

    /* background-color: var(--secondary-color); */
    background-color: white;
    width: 100%;
    height: var(--navbar-height);

    display: flex;
    align-items: center;
    justify-content: space-between;

    padding: 30px;
    box-sizing: border-box;

    -webkit-box-shadow:0px 81px 144px 6px rgba(62,66,66,0.09);
    -moz-box-shadow: 0px 81px 144px 6px rgba(62,66,66,0.09);
    box-shadow: 0px 81px 144px 6px rgba(62,66,66,0.09);

    z-index: 99;
}

nav .logo-holder img {
    width: auto;
    height: calc(var(--navbar-height) - 10px);

    
}

.sidebar {
    position: fixed;
    
    top:0;
    left:100%;

    background-color: white;

    height: 100vh;
    width: 100vw;
    
    display: flex;
    flex-direction: column;

    justify-content: flex-start;
    align-items: center;

    gap:15px;

    padding: 25px;
    box-sizing: border-box;
    transition: all 0.25s;
}
.extra-links{
    display: flex;
    flex-direction: column;

    justify-content: flex-start;
    align-items: center;

    gap:15px;

}
.sidebar-open{
    left: 0%;
}
.sidebar a,.sidebar p{
  text-decoration: none;
  font-size: 24px;
  font-weight: 700;
  color: #737373;
}
.icon-close-holder{
    width: 100%;

    display: flex;
    align-items: center;
    justify-content: flex-end;
    align-items: flex-start;

    flex-grow: 0.5;
}


</style>