<template>
    <p class="descr">Ещё одна фигура, с помощью которой можно выстраивать градиентный фон - это конус (будто мы смотрим на него сверху вниз), и задается такой фон с помощью свойства <b>conic-gradient</b>. 
    В скобках указываются цвета, используемые для градиента.
    <br><br>Попробуй задать конический градиентный фон из цветов #4D52FF, #FFFFFF и #8B18E5.
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