<template>
    <p class="descr"><b>background-size</b> - следующее на очереди свойство, отвечающее за размер фонового изображения. Очень часто размер картинки и размер блока, для которого она должна послужить фоном, не совпадают. Чтобы решить эту проблему, на помощь приходят пиксели, с помощью которых можно указать сначала ширину, а затем высоту. Например, <span class="example">background-size: 200px 500px;</span> изменит ширину фонового изображения на 200 пикселей, а высоту - на 500.
    <br><br>Попробуй указать размер фонового изображения 500 на 500 пикселей.
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
ul li{
    font-size: 18px;
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