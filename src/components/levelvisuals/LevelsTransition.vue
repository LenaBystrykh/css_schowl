<template>
    <div class="mainvisual">
        <div class="picture" v-bind:style="userStyle" v-bind:userValue="userValue" v-bind:currentlevel="currentlevel"><img class="pictureimg" src="../../../public/owl.png"></div>
    </div>
</template>
<script>
export default {
    props: {
        userStyle: {
            type: String,
            required: true
        },
        userValue: {
            type: String,
            required: true
        },
        currentlevel: {
            type: Object,
            required: true
        }
    }, 
}
</script>
<style scoped>
.mainvisual{
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
}
.picture{
    width: 40%;
    height: 46%;
    transition: 2s;
}
img{
    width: 100%;
}
.picture:hover{
    background-color: white;
    width: 80%;
    height: 92%;
}
</style>