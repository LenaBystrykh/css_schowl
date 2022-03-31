<template>
    <p class="descr">Финишная прямая по свойству <b>background-repeat</b>.
    <br>Какое значение нужно использовать, чтобы картинки заняли всё место, а если осталось свободное - растянулись, чтобы его заполнить?
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