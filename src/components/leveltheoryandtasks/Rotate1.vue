<template>
    <p class="descr"><b>Transform</b> - свойство, которое позволяет поворачивать, растягивать, наклонять и другими способами трансформировать элемент. Для данного свойства существует много различных значений для разных задач, поэтому разбирать будем постепенно. Начнём со значения <b>rotate</b>. Rotate позволяет поворачивать элемент на нужное количество градусов, или же можно указать желаемое количество поворотов. Можно записать значение с минусом для того, чтобы поворачивать элемент против часовой стрелки (от -360deg до -1deg) или без минуса, чтобы поворачивать по часовой стрелке. Для количества поворотов используется слово <b>turn</b>, например, <span class="example">transform: rotate(3turn);</span> полностью провернет элемент три раза.
    <br><br>
    Попробуй повернуть элемент на 70 градусов по часовой стрелке.
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
    font-size: 20px;
}
ul li{
    font-size: 20px;
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