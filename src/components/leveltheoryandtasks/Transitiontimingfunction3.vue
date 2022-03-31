<template>
    <p class="descr">Ещё один способ задать <b>transition-timing-function</b> - при помощи <a href="https://ru.wikipedia.org/wiki/Кривая_Безье" target="_blank">кривой Безье</a>. Такая кривая задаётся с помощью 4 точек, но первая и последняя точки всегда одинаковые - координаты первой = (0,0), а последней = (1,1). Поэтому эти точки указывать не нужно, а указываются только координаты второй и третьей. Например: <span class="example">transition-timing-function: cubic-bezier(0, 0, 0.58, 1.0);</span> соответствует значению ease-out, так как вторая точка совпадает с первой и тоже имеет координаты (0,0), а координаты третьей - (0.58,1). Значит, в начале переход происходит быстро - точки находятся в одном и том же месте, а дальше скорость замедляется. Важно, что все 4 значения должны быть не меньше 0 и не больше 1. Если тебе еще сложно разбираться с такими функциями, посмотри, как они работают при разных значениях, и вернись к этой теме, когда станешь немного постарше и дойдешь до более сложных тем в математике. Всё получится!
    <br><br>А пока примени кривую Безье для установки плавности анимации и укажи там точки с координатами (0.1, 0.45) и (0.9, 0.55).
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
a{
    text-decoration: none;
    color: rgb(255, 90, 0);
    font-weight: bold;
}
a:hover {
    color: black;
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