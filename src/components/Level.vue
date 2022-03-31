<template>
    <div class="level">
        <div class="prevBtn" @click="goPrev"><img src="../../public/left-arrow.png"></div>
        <div class="leveltitle">Уровень {{levelsamount.current}} / {{levelsamount.amount}}</div>
        <div class="nextBtn" @click="goNext"><img src="../../public/right-arrow.png"></div>
    </div>
</template>

<script>
import Visual from "./Visual"
export default {
    components: {
        Visual
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
        levelsamount: {
            type: Number,
            required: true
        }, 
        clearArea: {
            type: Boolean,
            required: true
        }
    },
    data() {
        return {
            newlevel: {
                topicnumber: 0, 
                topicname: '', 
                subtopicnumber: 0, 
                subtopicname: '', 
                levelinarray: 0, 
                level: 0,
                totalnumber: 0},
            newvisual: '',
            newtheory: '',
        }
    },
    methods: {
        goNext() {
            console.log(this.clearArea)
            if (this.levels[this.currentlevel.topicnumber].subtopic[this.currentlevel.subtopicnumber].levelnumbers.length > this.currentlevel.levelinarray + 1)
            {
                // go to the next level in this subtopic
                this.newlevel.topicnumber = this.currentlevel.topicnumber
                this.newlevel.topicname = this.currentlevel.topicname
                this.newlevel.subtopicnumber = this.currentlevel.subtopicnumber
                this.newlevel.subtopicname = this.currentlevel.subtopicname
                this.newlevel.levelinarray = this.currentlevel.levelinarray + 1
                this.newlevel.level = this.currentlevel.level + 1
                this.newlevel.totalnumber = this.currentlevel.totalnumber + 1
                this.newvisual = this.getVisual(this.newlevel.totalnumber)
                this.newtheory = this.newlevel.subtopicname + this.newlevel.level
                this.$emit('changelevel', this.newlevel)
                this.$emit('changevisual', this.newvisual)
                this.$emit('changetheory', this.newtheory)
                this.$emit('clearTextbox')
            }
            else
            {
                if (this.levels[this.currentlevel.topicnumber].subtopic.length > this.currentlevel.subtopicnumber + 1)
                {
                    // go to the first level of the next subtopic in this topic
                    this.newlevel.topicnumber = this.currentlevel.topicnumber
                    this.newlevel.topicname = this.currentlevel.topicname
                    this.newlevel.subtopicnumber = this.currentlevel.subtopicnumber + 1
                    this.newlevel.subtopicname = this.levels[this.currentlevel.topicnumber].subtopic[this.currentlevel.subtopicnumber + 1].name
                    this.newlevel.levelinarray = 0
                    this.newlevel.level = 1
                    this.newlevel.totalnumber = this.currentlevel.totalnumber + 1
                    this.newvisual = this.getVisual(this.newlevel.totalnumber)
                    this.newtheory = this.newlevel.subtopicname + this.newlevel.level
                    this.$emit('changevisual', this.newvisual)
                    this.$emit('changelevel', this.newlevel)
                    this.$emit('changetheory', this.newtheory)
                    this.$emit('clearTextbox')
                }
                else
                {
                    if (this.levels.length > this.currentlevel.topicnumber + 1) 
                    {
                        // go to the first level of the first subtopic in the next topic
                        this.newlevel.topicnumber = this.currentlevel.topicnumber + 1
                        this.newlevel.topicname = this.levels[this.currentlevel.topicnumber + 1].topic
                        this.newlevel.subtopicnumber = 0
                        this.newlevel.subtopicname = this.levels[this.currentlevel.topicnumber + 1].subtopic[0].name
                        this.newlevel.levelinarray = 0
                        this.newlevel.level = 1
                        this.newlevel.totalnumber = this.currentlevel.totalnumber + 1
                        this.newvisual = this.getVisual(this.newlevel.totalnumber)
                        this.newtheory = this.newlevel.subtopicname + this.newlevel.level
                        this.$emit('changevisual', this.newvisual)
                        this.$emit('changelevel', this.newlevel)
                        this.$emit('changetheory', this.newtheory)
                        this.$emit('clearTextbox')
                    }
                    else
                    {
                        console.log('листать некуда')
                    }
                }
            }
        },

        goPrev() {
            if (this.currentlevel.levelinarray - 1 >= 0)
            {
                // go to prev level in this subtopic
                this.newlevel.topicnumber = this.currentlevel.topicnumber
                this.newlevel.topicname = this.currentlevel.topicname
                this.newlevel.subtopicnumber = this.currentlevel.subtopicnumber
                this.newlevel.subtopicname = this.currentlevel.subtopicname
                this.newlevel.levelinarray = this.currentlevel.levelinarray - 1
                this.newlevel.level = this.currentlevel.level - 1
                this.newlevel.totalnumber = this.currentlevel.totalnumber - 1
                this.newvisual = this.getVisual(this.newlevel.totalnumber)
                this.newtheory = this.newlevel.subtopicname + this.newlevel.level
                this.$emit('changevisual', this.newvisual)
                this.$emit('changelevel', this.newlevel)
                this.$emit('changetheory', this.newtheory)
                this.$emit('clearTextbox')
            }
            else
            {
                if (this.currentlevel.subtopicnumber - 1 >= 0)
                {
                    // go to last level of the prev subtopic in this topic
                    this.newlevel.topicnumber = this.currentlevel.topicnumber
                    this.newlevel.topicname = this.currentlevel.topicname
                    this.newlevel.subtopicnumber = this.currentlevel.subtopicnumber - 1
                    this.newlevel.subtopicname = this.levels[this.currentlevel.topicnumber].subtopic[this.currentlevel.subtopicnumber - 1].name
                    this.newlevel.levelinarray = this.levels[this.currentlevel.topicnumber].subtopic[this.currentlevel.subtopicnumber - 1].levelnumbers.length - 1
                    this.newlevel.level = this.levels[this.currentlevel.topicnumber].subtopic[this.currentlevel.subtopicnumber - 1].levelnumbers.length
                    this.newlevel.totalnumber = this.currentlevel.totalnumber - 1
                    this.newvisual = this.getVisual(this.newlevel.totalnumber)
                    this.newtheory = this.newlevel.subtopicname + this.newlevel.level
                    this.$emit('changevisual', this.newvisual)
                    this.$emit('changelevel', this.newlevel)
                    this.$emit('changetheory', this.newtheory)
                    this.$emit('clearTextbox')
                }
                else
                {
                    if(this.currentlevel.topicnumber - 1 >= 0)
                    {
                        // go to the last level of last subtopic in the prev topic
                        this.newlevel.topicnumber = this.currentlevel.topicnumber - 1
                        this.newlevel.topicname = this.levels[this.currentlevel.topicnumber - 1].topic
                        this.newlevel.subtopicnumber = this.levels[this.currentlevel.topicnumber - 1].subtopic.length - 1
                        this.newlevel.subtopicname = this.levels[this.currentlevel.topicnumber - 1].subtopic[this.levels[this.currentlevel.topicnumber - 1].subtopic.length - 1].name
                        this.newlevel.levelinarray = this.levels[this.currentlevel.topicnumber - 1].subtopic[this.levels[this.currentlevel.topicnumber - 1].subtopic.length - 1].levelnumbers.length - 1
                        this.newlevel.level = this.levels[this.currentlevel.topicnumber - 1].subtopic[this.levels[this.currentlevel.topicnumber - 1].subtopic.length - 1].levelnumbers.length
                        this.newlevel.totalnumber = this.currentlevel.totalnumber - 1
                        this.newvisual = this.getVisual(this.newlevel.totalnumber)
                        this.newtheory = this.newlevel.subtopicname + this.newlevel.level
                        this.$emit('changevisual', this.newvisual)
                        this.$emit('changelevel', this.newlevel)
                        this.$emit('changetheory', this.newtheory)
                        this.$emit('clearTextbox')
                    }
                    else
                    {
                        console.log('листать некуда')
                    }

                }
            }
        },

        getVisual(levelnumber) {
            let levelvisualname = ''
            if (levelnumber >=1 && levelnumber <=7) {
                levelvisualname = 'LevelsMarginPadding'
            } else if (levelnumber >=8 && levelnumber <=26) {
                levelvisualname = 'LevelsBackground'
            } else if (levelnumber >=27 && levelnumber <=35) {
                levelvisualname = 'LevelsBackground2'
            } else if ((levelnumber >=36 && levelnumber <=43) || (levelnumber == 45)){
                levelvisualname = 'LevelsFlex'
            } else if (levelnumber == 44) {
                levelvisualname = 'LevelsFlexAlignItems'
            } else if (levelnumber == 46) {
                levelvisualname = 'LevelsFlexAlignContent'
            } else if (levelnumber == 47) {
                levelvisualname = 'LevelsFlexSelf'
            } else if (levelnumber == 48  || levelnumber == 51) {
                levelvisualname = 'LevelsFlexWrap1'
            } else if (levelnumber == 49) {
                levelvisualname = 'LevelsFlexWrap2'
            } else if (levelnumber == 50) {
                levelvisualname = 'LevelsFlexWrap3'
            } else if (levelnumber == 52) {
                levelvisualname = 'LevelsFlexGrow'
            } else if (levelnumber == 53 || levelnumber == 54) {
                levelvisualname = 'LevelsPosition'
            } else if (levelnumber == 55 || levelnumber == 56) {
                levelvisualname = 'LevelsPosition2'
            } else if (levelnumber >= 57 && levelnumber <= 66) {
                levelvisualname = 'LevelsTransform'
            } else if (levelnumber >= 67 && levelnumber <= 77) {
                levelvisualname = 'LevelsTransition'
            } else if (levelnumber >= 78 && levelnumber <= 88) {
                levelvisualname = 'LevelsAnimation'
            }
            return levelvisualname
        }
    }
}
</script>

<style scoped>
.level{
    display: flex;
    justify-content: center;
    align-items: center;
}
.leveltitle{
    font-size: 28px;
    width: 400px;
    background-color: rgb(255, 180, 0);
    padding: 8px 12px;
    border: none;
    border-radius: 12px;
    vertical-align: center;
    text-align: center;
}
img{
    width: 32px;
    height: 32px;
}

.nextBtn:active, .prevBtn:active{
    transform: scale(1.1);
}
</style>