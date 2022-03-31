<template>
    <p class="descr"><b>Background-color</b> - свойство, которое помогает выбрать цвет для фона элемента. Для установки подходящего цвета можно просто записать название этого цвета на английском языке, например <span class="example">background-color: red;</span> для выбора красного цвета.
    <br><br> Попробуй указать зеленый цвет фона (зеленый по-английски - green).
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
    font-size: 22px;
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