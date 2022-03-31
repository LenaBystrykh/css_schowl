<template>
    <div class="mainvisual" v-bind:style="userStyle" v-bind:userValue="userValue" v-bind:currentlevel="currentlevel">
        <div class="owlpicture">Здесь был совёнок, но он улетел по очень важным делам.</div>
        <div class="stickpicture">И забрал с собой свою веточку.</div>
        <div class="owlpicture">Второй совёнок спрятался.</div>
        <div class="stickpicture">Ветку тоже не забыл.</div>
        <div class="owlpicture">Здесь был совёнок, но он улетел по очень важным делам.</div>
        <div class="stickpicture">И забрал с собой свою веточку.</div>
        <div class="owlpicture">Второй совёнок спрятался.</div>
        <div class="stickpicture">Ветку тоже не забыл.</div>
        <div class="owlpicture">Здесь был совёнок, но он улетел по очень важным делам.</div>
        <div class="stickpicture">И забрал с собой свою веточку.</div>
        <div class="owlpicture">Второй совёнок спрятался.</div>
        <div class="stickpicture">Ветку тоже не забыл.</div>
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
    flex-wrap: wrap;
}
.owlpicture{
    width: 17%;
    height: 17%;
    /* display: flex;
    align-items: center; */
}
.stickpicture{
    width: 17%;
    height: 17%;
    /* display: flex;
    align-items: center; */
}
</style>