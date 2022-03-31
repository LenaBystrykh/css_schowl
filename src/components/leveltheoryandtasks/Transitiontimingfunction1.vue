<template>
    <p class="descr"><b>Transition-timing-function</b> - позволяет устанавливать то, насколько плавным будет переход в течение указанного времени: переход будет равномерным, или же более быстрым в начале и замедляться к концу, или он будет выполнен "шагами", в несколько этапов. Давай разберем их постепенно:
    <ul>
        <li><b>ease</b> - значение по умолчанию. Скорость увеличивается к середине перехода и замедляется к концу;</li>
        <li><b>ease-in</b> - начинается медленно, ускоряется к концу;</li>
        <li><b>ease-out</b> - начинается быстро, замедляется к концу;</li>
        <li><b>ease-in-out</b> - начинается медленно, в середине ускоряется, а к концу снова замедляется;</li>
        <li><b>linear</b> - весь переход выполняется равномерно.</li>
    </ul>Попробуй разные варианты!
    <br><br>А чтобы перейти на следующий уровень - настрой плавность перехода так, чтобы он начинался медленно, а затем набирал скорость.
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