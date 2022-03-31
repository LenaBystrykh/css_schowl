<template>
    <p class="descr">Напротив, если не нужно применять плавность ни к одному свойству, то есть совсем отменить это, можно указать значение <b>none</b> вместо перечисления нужных свойств.
    <br><br>Укажи его и посмотри, что теперь все свойства будут применяться сразу же.
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