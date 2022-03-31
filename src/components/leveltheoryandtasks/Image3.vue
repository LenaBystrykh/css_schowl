<template>
    <p class="descr">Ты делаешь успехи!
    <br>А какое же значение нужно для того, чтобы картинки заняли столько места, сколько смогут, но не обрезались и не растягивались?
    </p>
</template>

<script>
export default {

}
</script>

<style scoped>
.descr{
    width: 100%;
    height: fit-content;
    font-size: 24px;
}
span{
    background-color: rgb(255, 180, 0);
    border-radius: 5px; 
    padding: 0 5px;
}
.example{
    font-style: italic;
    background-color: rgb(255, 130, 0);
}
</style>