<template>
    <p class="descr"><b>background-size</b> содержит ещё несколько значений, позволяющих изменить размер фонового изображения и приблизить его к размеру элемента. Одно из них - <b>contain</b>. Оно увеличивает картинку, сохраняя пропорции. Если остаётся свободное место, оно может быть занято копиями этой картинки, если этому не мешает значение no-repeat. 
    <br><br>Попробуй посмотреть, как сможет измениться фоновая картинка при указании такого значения.
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