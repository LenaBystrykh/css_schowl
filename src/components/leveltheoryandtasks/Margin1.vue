<template>
    <p class="descr"><b>Margin</b> - свойство, отвечающее за расстояние от внешнего края элемента до других элементов. Сейчас края элементов обозначены белой рамкой, а расстояния между ними нет - они прижаты друг к другу. Для того, чтобы добавить это расстояние, необходимо к каждому элементу применить свойство margin и с помощью символа <span>:</span> указать нужное значение в пикселях(px - специальная единица измерения, если ты еще не знаешь про такую - почитай о ней в интернете), например, <span class="example">margin: 10px;</span><br><br>
    Попробуй указать внешние отступы между элементами по 20 пикселей.
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