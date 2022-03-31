<template>
    <p class="descr">Ещё один вариант изменения конического градиента - его "поворот": сейчас линия начала всегда выглядит <span>| так</span>, но это можно исправить, наклонив её с помощью команды <b>from</b> и указания количества градусов поворота в начале скобок. Например: <span class="example">background: conic-gradient(from 60deg, blue, violet, magenta);</span> "развернет" фон на 60 градусов.
    <br><br>Попробуй повернуть фон из уровня 9 на 120 градусов.
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
.example{
    font-style: italic;
    background-color: rgb(255, 130, 0);
}
</style>