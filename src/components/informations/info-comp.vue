<template>
    <div class="holder-info">
        <div class="icon">
            <slot name="Icon" ></slot>
        </div>
        <div class="text">
            <slot name="Information" ></slot>
        </div>

    </div>
</template>

<style scoped>
.holder-info{
    height: 100%;
    width: 100%;

    display: flex;
    flex-direction: row;
    flex-wrap: nowrap;
    justify-content: space-between;
    align-items: flex-start;

    background-color: white;

    gap: 10px;
    padding-top: 10px;
    padding-bottom: 10px;
    padding-left: 5vh;
    padding-right: 10px;
    box-sizing: border-box;
}
.text{
    height: 100%;
    width: 100%;
    
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: flex-start;

    padding-left:  15%;
    box-sizing: border-box;

    gap: 5px;

}
@media only screen and (max-width: 1000px) {
    .holder-info{
    gap: 10px;
    padding-top: 10px;
    padding-bottom: 10px;
    padding-left: 10px;
    padding-right: 10px;
}

}
</style>

