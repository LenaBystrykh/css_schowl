<template>
    <div class="mainvisual">
        <div class="owlpicture" v-bind:style="userStyle" v-bind:userValue="userValue" v-bind:currentlevel="currentlevel"></div>
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
    width: 100%;
    height: 100%;
    position: relative;
    transition: 1s;
    background: url("../../../public/owl.png");
    background-size: 23%;
    background-repeat: no-repeat;
}
</style>