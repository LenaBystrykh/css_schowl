<template>
    <p class="descr">Отлично справляешься! По-прежнему доступны только значения:
     <ul>
        <li><b>flex-start</b>;</li>
        <li><b>flex-end</b>;</li>
        <li><b>center</b>;</li>
        <li><b>space-between</b>;</li>
        <li><b>space-around</b>;</li>
        <li><b>space-evenly</b>.</li>
    </ul> 
    <br>Попробуй вспомнить, какое из них пригодится для того, чтобы расстояние между элементами было одинаковым, а до боковых стенок - чуть меньше.
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
ul li{
    font-size: 22px;
    list-style-type: disc;
    margin-left: 40px;
}
.example{
    font-style: italic;
    background-color: rgb(255, 130, 0);
}
</style>