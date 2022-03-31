<template>
    <p class="descr">Как для внутренних, так и для внешних отступов возникают ситуации, когда по бокам отступы одинаковые, а вот сверху и снизу отличаются и от боковых, и друг от друга. Можно так и указать <b>три</b> значения через пробел. Например, вместо того, чтобы расписывать <span>margin-top: 30px; margin-right: 20px; margin-bottom: 10px; margin-left: 20px;</span>, можно использовать уже знакомую форму записи: <span>margin: 30px 20px 10px 20px;</span>, а можно сократить и её: <span class="example">margin: 30px 20px 10px;</span>.<br><br>Попробуй попрактиковаться в последнем варианте: укажи <i>внутренние</i> отступы - сверху 50px, по бокам 15px, а снизу 5px.
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
    font-size: 22px;
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