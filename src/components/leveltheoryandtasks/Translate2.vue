<template>
    <p class="descr">Конечно же, может возникнуть необходимость совмещать свойства: и повернуть элемент, и сдвинуть его. Но в этом есть небольшая разница, и важно учитывать порядок, в котором указываются значения.
        Записываются они внутри одного свойства через пробел: <span class="example">transform: translate(-25%, 70px) rotate(3turn);</span>
        <br><br>
        Попробуй сейчас сначала сдвинуть элемент на 100 пикселей вправо и на 30 вниз, а затем повернуть на 90 градусов. 
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
    font-size: 20px;
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