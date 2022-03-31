<template>
    <div class="theory">
        <div class="top">
            <p class="title" v-bind:currentlevel="currentlevel" @changetheory="changetheory" @changelevel="changelevel"> {{currentlevel.topicname}} </p>
            <level v-bind:levels="levels" v-bind:clearArea="clearArea" v-bind:levelsamount="levelsamount" v-bind:currentlevel="currentlevel" v-bind:currentleveltheory="currentleveltheory" 
            v-bind:currentlevelvisual="currentlevelvisual" @clearTextbox="clearTextbox" @changetheory="changetheory" @changelevel="changelevel" @changevisual="changevisual"/>
        </div>
        <component v-bind:is="currentleveltheory"></component>
    </div>
</template>

<script>
import Level from "./Level"
import Margin1 from "./leveltheoryandtasks/Margin1"
import Margin2 from "./leveltheoryandtasks/Margin2"
import Margin3 from "./leveltheoryandtasks/Margin3"
import Margin4 from "./leveltheoryandtasks/Margin4"
import Padding1 from "./leveltheoryandtasks/Padding1"
import Padding2 from "./leveltheoryandtasks/Padding2"
import Padding3 from "./leveltheoryandtasks/Padding3"
import Color1 from "./leveltheoryandtasks/Color1"
import Color2 from "./leveltheoryandtasks/Color2"
import Color3 from "./leveltheoryandtasks/Color3"
import Color4 from "./leveltheoryandtasks/Color4"
import Gradient1 from "./leveltheoryandtasks/Gradient1"
import Gradient2 from "./leveltheoryandtasks/Gradient2"
import Gradient3 from "./leveltheoryandtasks/Gradient3"
import Gradient4 from "./leveltheoryandtasks/Gradient4"
import Gradient5 from "./leveltheoryandtasks/Gradient5"
import Gradient6 from "./leveltheoryandtasks/Gradient6"
import Gradient7 from "./leveltheoryandtasks/Gradient7"
import Gradient8 from "./leveltheoryandtasks/Gradient8"
import Gradient9 from "./leveltheoryandtasks/Gradient9"
import Gradient10 from "./leveltheoryandtasks/Gradient10"
import Gradient11 from "./leveltheoryandtasks/Gradient11"
import Gradient12 from "./leveltheoryandtasks/Gradient12"
import Gradient13 from "./leveltheoryandtasks/Gradient13"
import Gradient14 from "./leveltheoryandtasks/Gradient14"
import Gradient15 from "./leveltheoryandtasks/Gradient15"
import Image1 from "./leveltheoryandtasks/Image1"
import Image2 from "./leveltheoryandtasks/Image2"
import Image3 from "./leveltheoryandtasks/Image3"
import Image4 from "./leveltheoryandtasks/Image4"
import Image5 from "./leveltheoryandtasks/Image5"
import Image6 from "./leveltheoryandtasks/Image6"
import Image7 from "./leveltheoryandtasks/Image7"
import Image8 from "./leveltheoryandtasks/Image8"
import Image9 from "./leveltheoryandtasks/Image9"
import Flexdirection1 from "./leveltheoryandtasks/Flexdirection1"
import Flexdirection2 from "./leveltheoryandtasks/Flexdirection2"
import Justifycontent1 from "./leveltheoryandtasks/Justifycontent1"
import Justifycontent2 from "./leveltheoryandtasks/Justifycontent2"
import Justifycontent3 from "./leveltheoryandtasks/Justifycontent3"
import Justifycontent4 from "./leveltheoryandtasks/Justifycontent4"
import Justifycontent5 from "./leveltheoryandtasks/Justifycontent5"
import Alignitems1 from "./leveltheoryandtasks/Alignitems1"
import Alignitems2 from "./leveltheoryandtasks/Alignitems2"
import Alignitems3 from "./leveltheoryandtasks/Alignitems3"
import Aligncontent1 from "./leveltheoryandtasks/Aligncontent1"
import Alignself1 from "./leveltheoryandtasks/Alignself1"
import Flexwrap1 from "./leveltheoryandtasks/Flexwrap1"
import Flexwrap2 from "./leveltheoryandtasks/Flexwrap2"
import Flexwrap3 from "./leveltheoryandtasks/Flexwrap3"
import Flexflow1 from "./leveltheoryandtasks/Flexflow1"
import Flexgrow1 from "./leveltheoryandtasks/Flexgrow1"
import Relative1 from "./leveltheoryandtasks/Relative1"
import Absolute1 from "./leveltheoryandtasks/Absolute1"
import Fixed1 from "./leveltheoryandtasks/Fixed1"
import Sticky1 from "./leveltheoryandtasks/Sticky1"
import Rotate1 from "./leveltheoryandtasks/Rotate1"
import Rotate2 from "./leveltheoryandtasks/Rotate2"
import Translate1 from "./leveltheoryandtasks/Translate1"
import Translate2 from "./leveltheoryandtasks/Translate2"
import Translate3 from "./leveltheoryandtasks/Translate3"
import Scale1 from "./leveltheoryandtasks/Scale1"
import Skew1 from "./leveltheoryandtasks/Skew1"
import Skew2 from "./leveltheoryandtasks/Skew2"
import Matrix1 from "./leveltheoryandtasks/Matrix1"
import Matrix2 from "./leveltheoryandtasks/Matrix2"
import Transitionproperty1 from "./leveltheoryandtasks/Transitionproperty1"
import Transitionproperty2 from "./leveltheoryandtasks/Transitionproperty2"
import Transitionproperty3 from "./leveltheoryandtasks/Transitionproperty3"
import Transitionduration1 from "./leveltheoryandtasks/Transitionduration1"
import Transitiontimingfunction1 from "./leveltheoryandtasks/Transitiontimingfunction1"
import Transitiontimingfunction2 from "./leveltheoryandtasks/Transitiontimingfunction2"
import Transitiontimingfunction3 from "./leveltheoryandtasks/Transitiontimingfunction3"
import Transitiontimingfunction4 from "./leveltheoryandtasks/Transitiontimingfunction4"
import Transitiontimingfunction5 from "./leveltheoryandtasks/Transitiontimingfunction5"
import Transitiondelay1 from "./leveltheoryandtasks/Transitiondelay1"
import Transition1 from "./leveltheoryandtasks/Transition1"
import Animationname1 from "./leveltheoryandtasks/Animationname1"
import Animationduration1 from "./leveltheoryandtasks/Animationduration1"
import Animationtimingfunction1 from "./leveltheoryandtasks/Animationtimingfunction1"
import Animationdelay1 from "./leveltheoryandtasks/Animationdelay1"
import Animationiterationcount1 from "./leveltheoryandtasks/Animationiterationcount1"
import Animationiterationcount2 from "./leveltheoryandtasks/Animationiterationcount2"
import Animationdirection1 from "./leveltheoryandtasks/Animationdirection1"
import Animationdirection2 from "./leveltheoryandtasks/Animationdirection2"
import Animationdirection3 from "./leveltheoryandtasks/Animationdirection3"
import Animationfillmode1 from "./leveltheoryandtasks/Animationfillmode1"
import Animation1 from "./leveltheoryandtasks/Animation1"


export default {
    components: {
        Level, 
        Margin1, Margin2, Margin3, Margin4, Padding1, Padding2, Padding3, Color1, Color2, Color3, Color4,
        Gradient1, Gradient2, Gradient3, Gradient4, Gradient5, Gradient6, Gradient7, Gradient8, Gradient9, Gradient10, Gradient11, Gradient12, Gradient13, Gradient14, Gradient15,
        Image1, Image2, Image3, Image4, Image5, Image6, Image7, Image8, Image9,
        Flexdirection1, Flexdirection2, Justifycontent1, Justifycontent2, Justifycontent3, Justifycontent4, Justifycontent5,
        Alignitems1, Alignitems2, Alignitems3, Aligncontent1, Alignself1, Flexwrap1, Flexwrap2, Flexwrap3, Flexflow1, Flexgrow1,
        Relative1, Absolute1, Fixed1, Sticky1, Rotate1, Rotate2, Translate1, Translate2, Translate3, Scale1, Skew1, Skew2, Matrix1, Matrix2,
        Transitionproperty1, Transitionproperty2, Transitionproperty3, Transitionduration1, Transitiontimingfunction1, Transitiontimingfunction2,
        Transitiontimingfunction3, Transitiontimingfunction4, Transitiontimingfunction5, Transitiondelay1, Transition1,
        Animationname1, Animationduration1, Animationtimingfunction1, Animationdelay1, Animationiterationcount1, Animationiterationcount2, 
        Animationdirection1, Animationdirection2, Animationdirection3, Animationfillmode1, Animation1
    },
    props: {
        levels: {
            type: Array,
            required: true
        },
        currentlevel: {
            type: Object,
            required: true
        },
        currentlevelvisual: {
            type: String,
            required: true
        },
        currentleveltheory: {
            type: String,
            required: true
        },
        levelsamount: {
            type: Number,
            required: true
        },
        clearArea: {
            type: Boolean,
            required: true
        }
    },
    methods: {
        changelevel(lvl) {
            const newLevel = {
                topicnumber: lvl.topicnumber, 
                topicname: lvl.topicname, 
                subtopicnumber: lvl.subtopicnumber, 
                subtopicname: lvl.subtopicname, 
                levelinarray: lvl.levelinarray, 
                level: lvl.level,
                totalnumber: lvl.totalnumber
            }
            this.$emit('changelevel', newLevel)
            this.$emit('clearTextbox')
        },
        changevisual(visualname) {
            const newvisual = visualname
            this.$emit('changevisual', newvisual)
        },
        changetheory(theoryname) {
            const newtheory = theoryname
            this.$emit('changetheory', newtheory)
        }
    }
}
</script>

<style scoped>
.theory{
    display: flex;
    width: 100%;
    height: calc(50% - 20px);
    margin-bottom: 20px;
    justify-self: flex-start;
    flex-direction: column;
    background-color: rgb(255, 200, 0);
    padding: 8px 12px;
    border: none;
    border-radius: 8px;
}
.title{
    width: 100%;
    height: fit-content;
    font-size: 40px;
    font-weight: bold;
    font-family: 'Fredoka One', cursive;
}
.top{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    margin-bottom: 20px;
}
</style>