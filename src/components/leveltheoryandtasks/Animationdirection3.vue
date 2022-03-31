<template>
    <p class="descr">Молодец!
    <br>А теперь сделай плавную анимацию, которая будет воспроизводиться задом наперёд.
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
a{
    text-decoration: none;
    color: rgb(255, 90, 0);
    font-weight: bold;
}
a:hover {
    color: black;
}
ul li{
    font-size: 20px;
    list-style-type: disc;
    margin-left: 40px;
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