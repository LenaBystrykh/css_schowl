<template>
    <p class="descr">Так же, как и во внешних отступах margin, для внутренних отступов padding тоже есть 4 свойства, чтобы задавать разный размер отступов с разных сторон:
    <ul>
        <li><b>padding-top</b> для внутреннего отступа сверху,</li>
        <li><b>padding-right</b> для внутреннего отступа справа,</li>
        <li><b>padding-bottom</b> для внутреннего отступа снизу,</li>
        <li><b>padding-left</b> для внутреннего отступа слева.</li>
    </ul><br> Давай попробуем: укажи с помощью двух свойств внутренний отступ снизу в размере 20 пикселей, и внутренний отступ справа - 10 пикселей. 
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
ul li{
    font-size: 22px;
    list-style-type: disc;
    margin-left: 40px;
}
span{
    background-color: rgb(255, 180, 0);
    border-radius: 5px; 
    padding: 0 5px;
}
</style>