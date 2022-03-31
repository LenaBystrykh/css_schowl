<template>
    <p class="descr">Иногда нужно немножко подождать, прежде чем начать выполнять переход к новым стилям. В этом может помочь установление задержки - <b>transition-delay</b>. Так же, как и для длительности перехода, здесь указывается время в секундах. 
    <br><br>Установи задержку в 3 секунды перед началом перехода к новым стилям.
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