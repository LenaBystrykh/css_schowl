<template>
    <div>
    </div>
</template>

<script>
import LevelsMarginPadding from "./levelvisuals/LevelsMarginPadding"
import LevelsBackground from "./levelvisuals/LevelsBackground"
import LevelsBackground2 from "./levelvisuals/LevelsBackground2"
import LevelsFlex from "./levelvisuals/LevelsFlex"
import LevelsFlexWrap1 from "./levelvisuals/LevelsFlexWrap1"
import LevelsFlexWrap2 from "./levelvisuals/LevelsFlexWrap2"
import LevelsFlexWrap3 from "./levelvisuals/LevelsFlexWrap3"
import LevelsFlexGrow from "./levelvisuals/LevelsFlexGrow"
import LevelsPosition from "./levelvisuals/LevelsPosition"
import LevelsPosition2 from "./levelvisuals/LevelsPosition2"
import LevelsTransform from "./levelvisuals/LevelsTransform"
import LevelsTransition from "./levelvisuals/LevelsTransition"
import LevelsAnimation from "./levelvisuals/LevelsAnimation"
export default {
    components: {
        LevelsMarginPadding, 
        LevelsBackground,
        LevelsBackground2,
        LevelsFlex,
        LevelsFlexWrap1,
        LevelsFlexWrap2,
        LevelsFlexWrap3,
        LevelsFlexGrow,
        LevelsPosition,
        LevelsPosition2,
        LevelsTransform, 
        LevelsTransition,
        LevelsAnimation
    },
    props: {
        levels: {
            type: Array,
            required: true
        },
        currentlevel: {
            type: Array,
            required: true
        },
        currentlevelvisual: {
            type: String,
            required: true
        }
    },
    data() {
        return {
            newlevelvisual: 'LevelsMarginPadding'
        }
    },
    methods: {
        setVisual(value) {
            this.newlevelvisual = value;
            console.log(value)
    }
  }
}
</script>

<style scoped>

</style>