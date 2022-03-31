<template>
    <div class="mainvisual" v-bind:style="userStyle" v-bind:userValue="userValue" v-bind:currentlevel="currentlevel">
        <div class="picture"><img class="pictureimg" src="../../../public/owl.png"></div>
        <div class="picture"><img class="pictureimg" src="../../../public/owl2.png"></div>
        <div class="picture"><img class="pictureimg" src="../../../public/owl.png"></div>
        <div class="picture"><img class="pictureimg" src="../../../public/owl2.png"></div>
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
}
.picture{
    width: 17%;
}
img{
    width: 100%;
}
</style>