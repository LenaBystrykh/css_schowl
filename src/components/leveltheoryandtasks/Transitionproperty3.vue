<template>
    <p class="descr">Ну и последнее ключевое слово, которое может использоваться в <b>transition-property</b> - это <b>all</b>, оно также указывается вместо перечисления всех нужных свойств. 
    <br><br>Попробуй указать его и посмотри самостоятельно, к каким же свойствам элемента применится плавный переход?
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