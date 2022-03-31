<template>
    <p class="descr">Если указывать для <b>repeating-linear-gradient</b> точки перехода не в пикселях, а в процентах, то можно легче влиять на количество полос. Например: <span class="example">background: repeating-linear-gradient(45deg, orange, pink 50%);</span> создаст всего 2 градиентных полосы, а если вместо 50% указать 33.3% - их будет 3, 25% - 4 и так далее.
    <br><br>Попробуй изменить пример так, чтобы получился фон, состоящий из 10 полос.
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