<template>
    <p class="descr"><b>Animation</b> (анимация) немного похожа на переходы, однако разница состоит в том, что это гораздо более мощный инструмент, более подробно можно почитать <a href="https://cssanimation.rocks/ru/transition-vs-animation/" target="_blank">здесь</a>. Некоторые свойства похожи на <b>transition</b>, мы увидим это в следующих уровнях.
    Для того, чтобы создать анимацию, используются ключевые кадры:</p>
    <div class="explanation">
        <div class="left-explanation">
            <p class="descr">@keyframes isparenie {
                <br>    0% {
                    <br>        opacity: 1;
                <br>    }
                <br>    70% {
                    <br>        opacity: 0.5;
                <br>    }
                <br>    100% {
                    <br>        opacity: 0;
                <br>    }
                <br>}</p></div>
        <div class="right-explanation"><p class="descr">При создании анимации обязательно используется ключевое слово <b>@keyframes</b>, а затем указывается название созданной анимации, которое может быть совершенно любым, в данном случае - <i>isparenie</i>. Далее указываются ключевые кадры, их может быть любое количество, но обязательно должно присутствовать начало - 0% и конец - 100%. Для каждого ключевого кадра указываются желаемые свойства, которые нужно изменить на данном этапе. Всё это указывается <b>не внутри</b> стилей для элемента, а обычно - в самом конце документа со стилями. Соответственно, созданную анимацию можно применять уже для любого элемента. Чтобы это сделать, в стилях для конкретного элемента необходимо прописать <span class="example">animation-name: isparenie;</span>, где вместо <i>isparenie</i> указать название созданной анимации.</p></div></div>
    <br>
    <p class="descr">Нужная анимация уже создана и называется fly, попробуй применить её к элементу.
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
a{
    text-decoration: none;
    color: rgb(255, 90, 0);
    font-weight: bold;
}
a:hover {
    color: black;
}
.explanation{
    display: flex;
    width: 100%;
}
.left-explanation{
    background-color: rgb(255, 130, 0);
    font-style: italic;
    margin-right: 15px;
    width: 25%;
    height: fit-content;
}
.right-explanation{
    width: 75%;
}
.example{
    font-style: italic;
    background-color: rgb(255, 130, 0);
}
</style>