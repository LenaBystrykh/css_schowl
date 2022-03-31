<template>
    <p class="descr">Как и в радиальном градиенте, для конического можно сместить центр, используя слово <b>at</b> и значение по горизонтали и вертикали (в пикселях или процентах). Можно менять и пропорции цветов, указывая точки перехода в процентах.
    <br><br>Давай попрактикуемся. Укажи конический градиентный фон с центром, расположенным на 30% по горизонтали и на 70% по вертикали, и состоящий из цветов #4D52FF, #FFFFFF и #8B18E5 и с точками перехода 30%, 60% и 80% соответственно.
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