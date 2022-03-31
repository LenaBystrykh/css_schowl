<template>
    <p class="descr">Ура! Последнее, что мы научимся делать с анимацией - не записывать множество свойств для её настройки, а просто указать всё в одном свойстве <b>animation</b>. Порядок такой:
    <span>animation-name, animation-duration, animation-timing-function, animation-delay, animation-iteration-count, animation-direction, animation-fill-mode</span>. Пример: <span class="example">animation: jump 2s ease-in 1s 6 alternate backwards;</span> заставит элемент выполнять анимацию с названием <i>jump</i> 6 раз, каждый из которых длится по 2 секунды, переходы не будут заметны,  стили по окончании анимации сохранятся, анимация будет начинаться медленно и немного ускоряться к концу, а перед её началом пройдёт 1 секунда. 
    <br><br>Твоя очередь: примени анимацию с названием <i>round</i>, которая 1 повтор которой длится 10 секунд и повторяется она бесконечно в нормальном режиме, выполняется равномерно, задержка - 1 секунда, свойства сохраняются после окончания анимации.
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
a{
    text-decoration: none;
    color: rgb(255, 90, 0);
    font-weight: bold;
}
a:hover {
    color: black;
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