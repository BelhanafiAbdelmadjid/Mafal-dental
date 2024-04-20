<template>
    <div class="service-holder-card">
        <div class="holder-icon" >
            <div>
                <slot name="icon" ></slot>
            </div>
        </div>
        
        <p class="service-name">
            <slot name="TypeService"></slot>
        </p>
    </div>
</template>
<style scoped>
.holder-icon{
    width: 50%;
    height: 100%;

    display: flex;
    justify-content: center;
    align-items: center;

    
    padding: 10px;
    box-sizing: border-box;

    background-color: white;

    border-right: solid 1px var(--primary-color);
}


.service-holder-card{
    width: 100%;
    height: 80px;

    background-color: white;
    border-radius: 12px;

    display: flex;
    justify-content: space-between;
    align-items: center;

    overflow: hidden;
}

.service-holder-card .service-name{
    width: 100%;
    height: 100%;

    display: flex;
    justify-content: center;
    align-items: center;

    font-weight: 900;
    /* color: var(--break-color); */
    color: var(--gray-text-color);
}
</style>