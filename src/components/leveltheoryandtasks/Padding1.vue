<template>
    <p class="descr"><b>Padding</b> - свойство, отвечающее за расстояние от внутреннего края элемента до его содержимого. Сейчас на экране есть 4 одинаковых элемента, края которых обозначены белой рамкой. Внутри каждого из этих элементов находится картинка. Между картинкой и рамкой нет расстояния - отступы отсутствуют. Здесь всё устроено так же, как в margin: мы можем применить один общий отступ для всех элементов, но на этот раз уже внутри. Для этого нужно записать название свойства - <b>padding</b>, а затем через двоеточие указать нужный размер отступа: <span class="example">padding: 30px;</span> для внутреннего отступа в 30 пикселей.
    <br><br> Попробуй указать для элементов внутренние отступы по 10 пикселей. Не забудь про ; в конце строки.
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
    font-size: 22px;
}
ul li{
    font-size: 22px;
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