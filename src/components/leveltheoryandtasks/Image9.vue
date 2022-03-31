<template>
    <p class="descr">Последнее значение для <b>background-size</b>, которое мы рассмотрим - <b>cover</b>. Оно увеличивает картинку, сохраняя пропорции, так, чтобы не осталось свободного места. Зачастую это приводит к тому, что картинка обрезается, так как становится больше элемента. В таком случае иногда возникает необходимость также настроить положение картинки, чтобы была видна наиболее важная её часть. Именно для этого крайне часто используется комбинация <i>center/cover no-repeat</i> - чтобы одна картинка заняла весь элемент и разместилась по его центру.
    <br><br>Примени изученное значение для размера фонового изображения к текущему элементу.
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