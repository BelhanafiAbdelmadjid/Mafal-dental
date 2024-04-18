<template>
  <nav>
    <div class="logo-holder">
      <img src="../../assets/images/mafal-logo.png" alt="">
    </div>
    <div class="links">
      <slot name="links"></slot>
    </div>
  </nav>
</template>
<script>
</script>

<style scoped>
nav{
  position: sticky;
  left: 0;
  top: 0;

  /* background-color: var(--secondary-color); */
  background-color: white;
  width: 100%;
  height: var(--navbar-height);

  display: flex;
  align-items: center;
  justify-content: flex-start;

  padding: 30px;
  box-sizing: border-box;

  -webkit-box-shadow:0px 81px 144px 6px rgba(62,66,66,0.09);
  -moz-box-shadow: 0px 81px 144px 6px rgba(62,66,66,0.09);
  box-shadow: 0px 81px 144px 6px rgba(62,66,66,0.09);
}
nav .logo-holder{
  flex-grow: 0.25;
}
nav .logo-holder .logo{
  background-image: url();
  background-size: cover; 
  background-position: center center; 
  background-repeat: no-repeat; 
}
nav .logo-holder img{
  width: auto;
  height: calc(var(--navbar-height) - 10px);
}
nav .links{
  flex-grow: 0.5;

  font-weight: 900;

  display: flex;
  align-items: center;
  justify-content: flex-start;
  gap: 50px;
}

</style>