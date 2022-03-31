<template>
    <div class="mainvisual">
        <div id="self" v-bind:style="userStyle" v-bind:userValue="userValue" v-bind:currentlevel="currentlevel"><img class="pictureimg" src="../../../public/owl.png"></div>
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
<style>
.mainvisual{
    width: 100%;
    height: 100%;

}
#self{
    width: 17%;
    padding-top: 50%;
    position: relative;
    animation-duration: 4s;
    animation-iteration-count: infinite;
}
img{
    width: 100%;
}
@keyframes fly
{
    0%{
        bottom: 0px;
        left: 0px;
    }
    25%{
        bottom: 125px;
        left: 125px;
    }
    50%{
        bottom: 250px;
        left: 250px;
    }
    75%{
        bottom: 125px;
        left: 375px;
    }
    100%{
        bottom: 0px;
        left: 500px;
    }
}
@keyframes isparenie{
    0% {
        opacity: 1;
    }
    70% {
        opacity: 0.5;
    }
    100% {
        opacity: 0;
    }
}
@keyframes round{
    0% {
        transform: translateX(350px) rotate(0deg);
    }
    100%{
        transform: translateX(350px) rotate(359deg);
    }

}
</style>