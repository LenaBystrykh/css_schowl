<template>
    <p class="descr">А теперь что-то новенькое! Анимация может выполняться неоднократно. И для этого необходимо указать нужное количество повторов, используя свойство <b>animation-iteration-count</b>. Например, <span class="example">animation-iteration-count: 3;</span> заставит анимацию повториться 3 раза.
    <br><br>Попробуй настроить анимацию <i>fly</i> так, чтобы она повторялась полтора раза.
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