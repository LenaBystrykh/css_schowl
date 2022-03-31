<template>
    <p class="descr">Указывать наклон фона можно не только в градусах, но и с помощью специальных слов: <span>to top, to bottom, to left, to right</span> и их комбинаций. Также можно указывать через какое количество пикселей полосы будут повторяться. Например: <span class="example">background: repeating-linear-gradient(to top left, white, orange 200px);</span> создаст фон, где полоски будут располагаться / от правого нижнего угла до левого верхнего, каждая из которых будет занимать 200 пикселей.
    <br><br>Укажи повторяющийся фон из полосок розового, белого и красного цветов толщиной 250 пикселей в направлении влево.
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