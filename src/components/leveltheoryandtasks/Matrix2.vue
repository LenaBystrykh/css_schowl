<template>
    <p class="descr">Ну и финальное задание на трансформацию! Напоминаю порядок для <b>matrix</b>: <span>scaleX, skewY, skewX, scaleY, translateX, translateY</span>. 
    <br><br>
        Уменьши ширину в 2 раза, наклони элемент по оси Y на -0.5, а по У - на -0.2, увеличь высоту в полтора раза, и напоследок сдвинь всё это вправо на 10 пикселей и вниз на 20 пикселей. 
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