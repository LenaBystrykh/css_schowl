<template>
    <p class="descr"><b>Flex-flow</b> - свойство, которое объединяет в себе flex-direction и flex-wrap. Значения указываются через пробел, например: <span class="example">flex-flow: column wrap;</span> размещает элементы в столбик и переносит на следующий столбец те элементы, которые не вмещаются в столбец.
    <br><br>Примени это свойство для того, чтобы выстроить элементы в строку в обратном порядке и отключить перенос на следующую строку. <i>Не забудь включить флекс</i></p>
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
ul li{
    font-size: 17px;
    list-style-type: disc;
    margin-left: 40px;
}
.example{
    font-style: italic;
    background-color: rgb(255, 130, 0);
}
</style>