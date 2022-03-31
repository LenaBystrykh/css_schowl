<template>
    <p class="descr"><b>Flex-grow</b> - свойство, позволяющее элементам расти. По умолчанию его значение 0. Если элементы занимают не всю ширину родительского блока и одному из них указать flex-grow: 1, то он займет всё оставшееся место. Если же одному элементу из трёх задать значение flex-grow: 1, второму - 2, а третьему - 3, то вся ширина разделится на 6 частей и первый элемент займет одну такую часть, второй - две, а третий - три. 
    <br><br>Примени это свойство для того, чтобы элемент занял всё свободное место.</p>
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