<template>
    <p class="descr"><b>Align-content</b> выполняет ту же функцию, что и <b>align-items</b>, но вся разница в том, что первое свойство применяется в том случае, если элементы содержат несколько строк текста. Если же элементы однострочные, то следует использовать align-items. 
    <br><br>Для прохождения на следующий уровень включи флекс и примени свойство для выравнивания многострочных элементов по центру. Но перед этим можешь посмотреть разницу со свойством для однострочных элементов.
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