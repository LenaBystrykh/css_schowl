<template>
    <p class="descr"> Указать разные расстояния можно и с помощью одного общего свойства <b>margin</b>. Значения указываются через пробел в следующем порядке: <b>верх, право, низ, лево</b>.
    <br><br> Укажи внешние отступы от верхнего края на 15 пикселей, от правого и нижнего на 30 пикселей. Отступ от левого края не нужен (он будет равен 0 пикселей).
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
</style>