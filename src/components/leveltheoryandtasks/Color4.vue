<template>
    <p class="descr">Кроме того, цвет можно задавать в формате <b>HSL</b>. По аналогии с rgb - rgba есть также формат <b>HSLA</b> с указанием непрозрачности, о нем мы и поговорим. HSL - сокращение от Hue, Saturation, Lightness: 
    <ul>
        <li><b>Hue (цвет/оттенок)</b> указывается от 0 до 360 и отвечает за цвет - как будто мы двигаем вертикальную полоску выбора цвета на <a href="https://htmlcolorcodes.com/" target="_blank">том самом сайте</a>, где 0 - красный, вверху, а чем ниже спускаемся, тем больше число (в конце снова красный и после 360 сразу 0).</li>
        <li><b>Saturation (насыщенность)</b> - то, в какой части квадрата выбора оттенка мы находимся. 100% - справа, все цвета очень яркие и насыщенные, 0% - слева, можешь заметить, что в левой части квадрата расположены оттенки серого цвета, там нет никакой насыщенности цвета.</li>
        <li><b>Lightness (светлота/темнота)</b>, здесь тоже указывается значение от 0% до 100%, где 0% - самый светлый цвет, белый, а 100% - это самый темный цвет, черный.</li>
    </ul>
    Пример: оранжевый цвет будет задаваться первым параметром и принимать значение около 40, можно сделать его не полностью насыщенным, указав второму параметру значение 80%, и сказать, что он будет больше светлый, чем темный - к примеру, на 70%. Также можно указать непрозрачность 80% - через этот цвет будет слегка видно содержимое позади. <span class="example">background-color: hsla(40, 80%, 70%, 0.8);</span>
    <br><br> Попрактикуйся и укажи светло-розовый почти прозрачный фон через hsla. Используй значение цвета 300, насыщенность 15%, светлоту 90%, а непрозрачность - всего 30%.
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
    font-size: 18px;
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
ul li{
    font-size: 18px;
    list-style-type: disc;
    margin-left: 40px;
}
a{
    text-decoration: none;
    color: rgb(255, 90, 0);
    font-weight: bold;
}
a:hover {
    color: black;
}
</style>