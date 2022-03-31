<template>
    <p class="descr">Отлично! Получилось добавить одинаковое расстояние между всеми элементами. Но на самом деле можно задавать и разные отступы с разных сторон. В этом помогают четыре свойства:
        <ul>
                <li><strong>margin-top</strong> - расстояние от верхнего края,</li>
                <li><strong>margin-right</strong> - расстояние от правого края,</li>
                <li><strong>margin-bottom</strong> - расстояние от нижнего края,</li>
                <li><strong>margin-left</strong> - расстояние от левого края.</li>
            </ul>
        Для того, чтобы их применить, нужно точно так же записать нужное свойство, а затем через символ <span>:</span> значение в пикселях. Каждое свойство записывается в отдельной строке. Не забывай про символ <span>;</span> в конце строки.<br><br>
        Настрой отступы так, чтобы у элементов добавилось расстояние в 15 пикселей от левого края и 50 пикселей от нижнего края.
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
</style>