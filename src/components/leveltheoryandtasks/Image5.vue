<template>
    <p class="descr">Вот мы и подошли к следующему свойству для работы с картинками на фоне - <b>background-position</b>. Оно указывает, где именно будет находиться изображение. 
    Положение можно указывать словами: top, right, bottom, left, center. Можно сделать это с помощью процентов: <span class="example">background-position: 60% 30%;</span> сдвинет изображение чуть правее и выше середины экрана. А можно указывать положение прямо пикселями.
    <br><br> Укажи такое расположение фонового изображения, чтобы оно располагалось в 50 пикселях от левого края и в 60% - от верхнего.
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