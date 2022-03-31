<template>
    <p class="descr">Свойство <b>animation-delay</b> позволяет задать задержку перед началом выполнения анимации. Время указывается в секундах.
    <br><br>Сделай так, чтобы анимация <i>isparenie</i> запустилась только через 4 секунды.
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