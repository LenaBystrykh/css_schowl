<template>
    <p class="descr">Ну и последнее значение - это <b>wrap-reverse</b>. Со словом <i>reverse</i> мы уже сталкивались в других свойствах.
    <br><br>Так что примени его и посмотри, для чего оно используется.</p>
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