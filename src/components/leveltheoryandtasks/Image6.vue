<template>
    <p class="descr">Молодец! Давай закрепим два изученных свойства: <b>background-repeat</b> и <b>background-position</b>. 
    <br><br>Попробуй указать, что изображение будет размещаться слева внизу, но при этом, чтобы оно выстроилось в строчку, повторялось.
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
ul li{
    font-size: 18px;
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