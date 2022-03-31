<template>
    <p class="descr"><b>Skew</b> отвечает за деформацию элемента. Аналогично:
    <ul>
        <li><b>skewX</b> - деформирует стороны элемента по горизонтали;</li>
        <li><b>skewY</b> - деформирует стороны элемента по вертикали;</li>
        <li><b>skew</b> - деформирует элемент во все стороны.</li>
    </ul>Если рассмотреть <b>skewX</b> подробнее, то можно заметить, что он деформирует стороны элемента относительно оси Х - углы от 0 до 90 или от -180 до -90 градусов растягивают элемент <span>вот так \</span> и до <span>_ влево</span>, от -90 до 0 или от 90 до 180 <span>вот так /</span> и до <span>_ вправо</span>. Обязательно попробуй вводить разные значения и посмотреть, как будет меняться элемент.
    <br><br>Ну а после того, как попробуешь достаточно вариантов, сделай так, чтобы элемент будто слегка наклонился вправо: на 30 градусов /.
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