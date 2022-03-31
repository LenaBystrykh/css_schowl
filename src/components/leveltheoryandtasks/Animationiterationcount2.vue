<template>
    <p class="descr">А для того, чтобы анимация повторялась постоянно, пока работает сайт, для свойства <b>animation-iteration-count</b> необходимо указать значение <i>infinite</i>, то есть <i>бесконечный</i>.
    <br><br>Так и сделай, пусть анимация <i>fly</i> воспроизводится без остановки!
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