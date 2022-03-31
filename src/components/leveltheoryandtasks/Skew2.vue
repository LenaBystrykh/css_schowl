<template>
    <p class="descr"><b>SkewX</b> деформирует стороны элемента относительно оси Х - углы от 0 до 90 или от -180 до -90 градусов растягивают элемент <span>вот так \</span> и до <span>_ влево</span>, от -90 до 0 или от 90 до 180 <span>вот так /</span> и до <span>_ вправо</span>. <b>SkewY</b> делает то же самое, но относительно оси У: углы от 0 до 90 или от -180 до -90 градусов растягивают элемент <span>вот так \</span> и до <span>| вправо</span>, от -90 до 0 или от 90 до 180 <span>вот так /</span> и до <span>| влево</span>. Настоятельно рекомендую проверить и это! <b>Skew</b>, в свою очередь, совмещает оба свойства, например, <span class="example">transform: skew(50deg, -20deg);</span> почти положит элемент на бок \. 
    <br><br>Попробуй деформировать элемент на 10 градусов по оси Х и на 10 градусов по оси У.
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