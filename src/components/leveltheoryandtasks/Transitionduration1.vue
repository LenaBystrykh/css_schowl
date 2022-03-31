<template>
    <p class="descr"><b>Transition-duration</b> - ещё одно свойство, относящееся к transition. Оно позволяет устанавливать длительность этого перехода. На прошлых трех уровнях она уже была установлена автоматически: изменения применялись за 2 секунды: <span class="example">transition-duration: 2s;</span>. Здесь можно указывать любое время в секундах. Причём, если в <b>transition-property</b> перечислялись несколько свойств, можно задать разную длительность перехода к каждому из них: <span class="example">transition-property: width, height;<br>transition-duration: 3s, 0.5s;</span>. 
    <br><br>Укажи время применения новых свойств - 4 секунды.
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