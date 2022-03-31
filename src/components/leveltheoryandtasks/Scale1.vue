<template>
    <p class="descr"><b>Scale</b> отвечает за растягивание элементов. Здесь тоже существует несколько возможностей:
    <ul>
        <li><b>scaleX</b> - растягивает элемент по горизонтали;</li>
        <li><b>scaleY</b> - растягивает элемент по вертикали;</li>
        <li><b>scale</b> - совмещает scaleX и scaleY, в скобках указывается два значения через запятую (именно в таком порядке).</li>
    </ul> В данном случае в скобках располагается число: во сколько раз элемент должен стать больше, причём можно использовать нецелые числа. Если же элемент нужно уменьшить, указывается нецелое число от 0 до 1. Например, <span class="example">transform: scaleX(0.2);</span> уменьшит элемент в 5 раз по ширине, высота останется прежней.
    <br><br>Твоя задача: заставить элемент подрости. А именно - сделать его выше в 2 раза и уменьшить его ширину в 2 раза.
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