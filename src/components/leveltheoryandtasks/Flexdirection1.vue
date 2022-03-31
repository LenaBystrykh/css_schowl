<template>
    <p class="descr">Для управления расположением блоков на странице и их взаимоотношением используется <b>flex</b>. Он относится к типам отображения, поэтому, чтобы начать применять его свойства, необходимо его "включить", прописав <span class="example">display: flex;</span>Flex содержит множество свойств и значений, давай приступим к их изучению! Первым свойством, которое мы рассмотрим, будет <b>flex-direction</b>. Данное свойство используется для того, чтобы задать направление элементов:
    <ul>
        <li><b>row</b> - в строчку;</li>
        <li><b>column</b> - в столбик;</li>
        <li><b>row-reverse</b> - в строчку в обратном порядке;</li>
        <li><b>column-reverse</b> - в столбик в обратном порядке.</li>
    </ul> По умолчанию все элементы выстраиваются в строчку.
    <br><br>Давай попробуем переставить их задом наперед! Пусть они выстроятся в обратном порядке.
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
ul li{
    font-size: 22px;
    list-style-type: disc;
    margin-left: 40px;
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