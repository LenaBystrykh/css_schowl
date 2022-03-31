<template>
    <div class="mainvisual">
        <div class="item" v-bind:style="userStyle" v-bind:userValue="userValue" v-bind:currentlevel="currentlevel"><img src="../../../public/owlart.jpg"></div>
        <div class="item" v-bind:style="userStyle" v-bind:userValue="userValue" v-bind:currentlevel="currentlevel"><img src="../../../public/owlart.jpg"></div>
        <div class="item" v-bind:style="userStyle" v-bind:userValue="userValue" v-bind:currentlevel="currentlevel"><img src="../../../public/owlart.jpg"></div>
        <div class="item" v-bind:style="userStyle" v-bind:userValue="userValue" v-bind:currentlevel="currentlevel"><img src="../../../public/owlart.jpg"></div>
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
    display: flex;
    flex-wrap: wrap;
    width: 100%;
    height: 100%;
    box-sizing: border-box;
}
.item{
    width: 50%;
    height: 50%;
    border: 5px solid white;
}
img{
    width: 100%;
    height: stretch;
}
</style>
        