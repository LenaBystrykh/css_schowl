<template>
    <p class="descr">Отлично! Следующий набор значений для <b>transition-timing-function</b>:
    <ul>
        <li><b>step-start</b> - все применяемые свойства сразу же принимают новое значение, в 1 "шаг" в начале;</li>
        <li><b>step-end</b> - свойства находятся в своем прежнем значении на протяжении всей длительности перехода, и в последний момент сразу принимают новые значения, в 1 "шаг" в конце.</li>
    </ul>
    <br>Укажи применение свойств в один момент в самом начале перехода.
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
    font-size: 24px;
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