<template>
    <div class="holder">
        <p>PROFESSIONNEL</p>
        <p class="ligne"></p>
        <p>DENTISTE</p>
    </div>
</template>
<style scoped>
.holder{
    width: auto;
    height: auto;

    display: flex;
    justify-content: space-between;
    align-items: center;

    gap: 20px;

    color:  var(--secondary-color);

    background-color: var(--primary-color);


    padding-left: 20px;
    padding-right: 20px;
    padding-top: 3px;
    padding-bottom: 3px;
    box-sizing: border-box;

    border-radius: 20px;
    font-weight: 500;

}
.holder .ligne{
    width: 50px;
    height: 2px;
    background-color: var(--details-color);
}
@media only screen and (max-width: 600px) {
    .holder {
            font-size: 12px;
            gap: 10px;
    
            padding-left: 10px;
            padding-right: 10px;
            padding-top: 3px;
            padding-bottom: 3px;
            box-sizing: border-box;
    
            border-radius: 20px;
            font-weight: 500;
        }
}
</style>