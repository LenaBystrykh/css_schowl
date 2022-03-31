<template>
    <p class="descr">Если нужен полосатый фон, конечно же, никто не станет указывать цвета столько раз, сколько должно быть полосок. Это можно сделать спомощью свойства <b>repeating-linear-gradient</b>, то есть, повторяющийся линейный градиент. В нём тоже можно указать угол наклона полосок, а затем набор цветов, которые должны использоваться, и точки перехода (они определят расстояние между линиями, их толщину).
    Например: <span class="example">background: repeating-linear-gradient(130deg, white 0px, white 40px, orange 70px, orange 100px);</span> создаст бело-оранжевый полосатый фон.
    <br><br>Попробуй указать повторяющийся фон из красных и розовых полосок под углом 60 градусов, где красная часть занимает расстояние от 10 до 20 пикселей, а розовая - от 40 до 80.
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