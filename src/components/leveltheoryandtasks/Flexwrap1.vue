<template>
    <p class="descr">Следующее свойство флекса - <b>flex-wrap</b>, отвечает за переносы элементов на следующую строку/столбец, если они не вмещаются. По умолчанию при применении флекса для данного свойства стоит значение <b>nowrap</b>, то есть без переносов - флекс умещает всё в одну строку, а если не влезает - сжимает.
    <br><br>Проверь: задай флекс, можешь принудительно использовать свойство flex-wrap со значением nowrap.</p>
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