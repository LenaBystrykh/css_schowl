<template>
    <p class="descr"><b>Align-self</b> делает то же самое, что и <b>align-items</b> - выравнивает по вспомогательной оси, но теперь уже не все элементы внутри, а сам элемент. Соответственно, если раньше все флекс-свойства прописывались в родительском элементе и оттуда управляли внутренними элементами, то align-self задается уже внутри того элемента, который необходимо выровнять.
    <br><br>Попробуй указать элементу нужное свойство и значение, чтобы сместить только его в начало.</p>
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
ul li{
    font-size: 17px;
    list-style-type: disc;
    margin-left: 40px;
}
.example{
    font-style: italic;
    background-color: rgb(255, 130, 0);
}
</style>