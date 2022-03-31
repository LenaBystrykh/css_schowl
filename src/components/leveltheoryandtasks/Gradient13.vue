<template>
    <p class="descr">Но повторяющиеся фоны - не обязательно полосатые. Радиальные и конические фоны тоже могут содержать повторы, и для этого используются <b>repeating-radial-gradient</b> или <b>repeating-conic-gradient</b>. Точно так же внутри необходимо указывать цвета, которые будут повторяться, и расстояния между ними.
    <br><br>Укажи повторяющийся радиальный фон, где красный цвет (red) используется от 0 до 50 пикселей, а розовый (pink) - от 50 до 100 пикселей.
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