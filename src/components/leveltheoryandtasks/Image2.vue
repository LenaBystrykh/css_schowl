<template>
    <p class="descr">Молодец! 
    <br>Теперь попробуй выстроить изображения на фоне так, чтобы они повторялись во все стороны, занимая весь элемент, а если не влезают - обрезались.
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