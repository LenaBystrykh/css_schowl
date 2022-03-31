<template>
    <p class="descr">Вот мы и добрались до главного свойства - <b>transition</b>. Оно объединяет в себе все пройденные свойства переходов. Вместо того, чтобы указывать их отдельно, можно использовать одно общее свойство. Порядок следующий: <span>transition-property, transition-duration, transition-timing-function, transition-delay</span>. Например: для применения перехода ко всем свойствам элемента в течение 5 секунд с равномерной скоростью и задержкой 1 секунду можно указать <span class="example">transition: all, 5s, linear, 1s;</span>.
    <br><br>Установи с помощью одного свойства задержку в 0.5 секунд перед переходом длительностью 3 секунды для ширины элемента за 4 шага, первый из которых совершается в самом начале перехода.
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
a{
    text-decoration: none;
    color: rgb(255, 90, 0);
    font-weight: bold;
}
a:hover {
    color: black;
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