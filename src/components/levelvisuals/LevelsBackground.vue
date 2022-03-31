<template>
    <div class="mainvisual">
        <div class="owlpicture"><img src="../../../public/owl.png"></div>
        <div class="bg" v-bind:style="userStyle" v-bind:userValue="userValue" v-bind:currentlevel="currentlevel"></div>
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
    }
}
</script>
<style scoped>
.mainvisual{
    width: 100%;
    height: 100%;
    position: relative;
}
.owlpicture{
    opacity: 1;
    z-index: 2;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    transition: 1s;
}
.owlpicture:hover{
    opacity: 0;
}
.bg{
    width: 100%;
    height: 100%;
    position: absolute;
    top: 0;
    left: 0;
    opacity: 0.8;
    z-index: 1;
}
</style>