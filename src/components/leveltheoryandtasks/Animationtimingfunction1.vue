<template>
    <p class="descr">Следующее свойство - плавность анимации - <b>animation-timing-function</b>. Работает точно так же, как и timing-function для переходов, можешь повторить: это уровни 5-9 в главе "переходы". Все возможные значения абсолютно совпадают! Давай повторим их.
    <br><br> Задай анимацию <i>fly</i> и укажи ей плавность так, чтобы она начиналась медленно, к середине ускорялась а затем снова замедлялась к концу.
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
a{
    text-decoration: none;
    color: rgb(255, 90, 0);
    font-weight: bold;
}
a:hover {
    color: black;
}
.example{
    font-style: italic;
    background-color: rgb(255, 130, 0);
}
</style>