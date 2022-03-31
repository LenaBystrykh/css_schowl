background: linear-gradient(90deg, rgba(255, 255, 0, 0.5), rgba(255, 150, 0, 0.5), rgba(255, 170, 233, 0.5)), url("https://cdn-icons-png.flaticon.com/512/1864/1864652.png" ) center/cover no-repeat;
<template>
    <p class="descr">Теперь попробуй самостоятельно указать фон из двух частей: первый - линейный градиент из трёх цветов под углом 90 градусов. Первый цвет в rgb - 255, 255, 0. Второй цвет - 255, 150, 0. Третий - 255, 170, 230. Также укажи 50% непрозрачности для всех цветов. Вторая часть фона - картинка! Так она будто бы спрячется позади градиента. Для использования изображения на фоне понадобится указать <b>url</b>, а внутри в скобках - ссылку на изображение в кавычках. Пропиши после указания градиента следующее значение: <span>url("https://cdn-icons-png.flaticon.com/512/1864/1864652.png") center/cover no-repeat</span>. Так ты укажешь нужную картинку, и разместишь её по центру экрана на весь размер блока. Более подробно мы изучим использование картинок для фона на следующем уровне, удачи!
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
.example{
    font-style: italic;
    background-color: rgb(255, 130, 0);
}
</style>