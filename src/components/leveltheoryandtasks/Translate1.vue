<template>
    <p class="descr">Замечательно, с поворотами разобрались. Перейдем к <b>translate</b>. Translate позволяет двигать элемент: вверх, вправо, вниз, влево. Как? При помощи значений:
        <ul>
            <li><strong>translateX</strong> - сдвиг элемента по горизонтали: влево или вправо;</li>
            <li><strong>translateY</strong> - сдвиг элемента по вертикали: вверх или вниз;</li>
            <li><strong>translate</strong> - общее значение, объединяющее в себе translateX и translateY, движение во все стороны.</li>
        </ul>
        Для того, чтобы их применить, нужно записать в скобках после значения то, насколько необходимо сдвинуть элемент. Это можно сделать в пикселях или процентах. Пример: <span class="example">transform: translateX(30px);</span>, чтобы сдвинуть элемент на 30 пикселей вправо. Укажешь значение с минусом - сдвинется влево. Точно так же: положительное число в translateY - движение вниз, отрицательное - вверх. <span class="example">transform: translate(20%, -70px);</span> сдвинет элемент на 20% вправо и на 70 пикселей вверх. 
        <br><br>
        Воспользуйся <i>одним</i> свойством и попробуй сдвинуть элемент на 50 пикселей влево и на 40% вверх.
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