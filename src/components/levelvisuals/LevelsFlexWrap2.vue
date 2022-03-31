<template>
    <div class="mainvisual">
        <div class="owls" v-bind:style="userStyle" v-bind:userValue="userValue" v-bind:currentlevel="currentlevel">
            <div class="picture"><img class="pictureimg" src="../../../public/owl.png"></div>
            <div class="picture"><img class="pictureimg" src="../../../public/owl2.png"></div>
            <div class="picture"><img class="pictureimg" src="../../../public/owl2.png"></div>
            <div class="picture"><img class="pictureimg" src="../../../public/owl2.png"></div>
            <div class="picture"><img class="pictureimg" src="../../../public/owl.png"></div>
            <div class="picture"><img class="pictureimg" src="../../../public/owl.png"></div>
            <div class="picture"><img class="pictureimg" src="../../../public/owl2.png"></div>
            <div class="picture"><img class="pictureimg" src="../../../public/owl.png"></div>
            <div class="picture"><img class="pictureimg" src="../../../public/owl2.png"></div>
            <div class="picture"><img class="pictureimg" src="../../../public/owl2.png"></div>
        </div>
        <div class="sticks">
            <div class="picture"><img class="pictureimg" src="../../../public/stick2.png"></div>
            <div class="picture"><img class="pictureimg" src="../../../public/stick2.png"></div>
            <div class="picture"><img class="pictureimg" src="../../../public/stick2.png"></div>
            <div class="picture"><img class="pictureimg" src="../../../public/stick2.png"></div>
            <div class="picture"><img class="pictureimg" src="../../../public/stick2.png"></div>
            <div class="picture"><img class="pictureimg" src="../../../public/stick2.png"></div>
            <div class="picture"><img class="pictureimg" src="../../../public/stick2.png"></div>
            <div class="picture"><img class="pictureimg" src="../../../public/stick2.png"></div>
            <div class="picture"><img class="pictureimg" src="../../../public/stick2.png"></div>
            <div class="picture"><img class="pictureimg" src="../../../public/stick2.png"></div>
        </div>
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
    position: relative;
}
.picture{
    width: 17%;
}
.owls{
    position: absolute;
    z-index: 2;
}
.sticks{
    position: absolute;
    top: 10%;
    display: flex;
    flex-wrap: wrap;
    z-index: 1;
}
.sticks img{
    padding-bottom: 25%;
}
img{
    width: 100%;
}
</style>