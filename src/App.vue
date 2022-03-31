<template>
    <div class="application">
        <div class="main" v-if="mainpage === true">
            <h1 class="header">Css schowl</h1>
            <ul>
                <li class="topic-item item1" @click="chooseTopic">1 глава<br>Отступы</li>
                <li class="topic-item item2" @click="chooseTopic">2 глава<br>Фон</li>
                <li class="topic-item item3" @click="chooseTopic">3 глава<br>Выравнивание</li>
                <li class="topic-item item4" @click="chooseTopic">4 глава<br>Позиция</li>
                <li class="topic-item item5" @click="chooseTopic">5 глава<br>Трансформация</li>
                <li class="topic-item item6" @click="chooseTopic">6 глава<br>Переходы</li>
                <li class="topic-item item7" @click="chooseTopic">7 глава<br>Анимация</li>
            </ul>
        </div>
        <div v-else class="levelpage">
            <div class="left">
                <button class="back-btn" @click="backToMain"><img src="../public/back.png"><p>К темам</p></button>
                <theory v-bind:levels="levels" v-bind:clearArea="clearArea" v-bind:levelsamount="levelsamount" v-bind:currentlevel="currentlevel" v-bind:currentlevelvisual="currentlevelvisual" v-bind:currentleveltheory="currentleveltheory" 
                @clearTextbox="clearTextbox" @changetheory="changetheory" @changelevel="changelevel" @changevisual="changevisual"/>
                <coding v-bind:numbers="numbers" v-bind:clearArea="clearArea" v-bind:codes="codes" v-bind:levels="levels" @create="checkCss" v-bind:correctAnswer="correctAnswer" v-bind:currentlevel="currentlevel" v-bind:currentlevelvisual="currentlevelvisual" :clearArea="clearArea" @unclear="unclear" @changetheory="changetheory" @changelevel="changelevel" @changevisual="changevisual" />
            </div>
            <div class="right">
                <component v-bind:is="currentlevelvisual" v-bind:userStyle="userStyle" v-bind:userValue="userValue" v-bind:currentlevel="currentlevel"></component>
            </div>
        </div>
    </div>
</template>

<script>
import Theory from "./components/Theory"
import Coding from "./components/Coding"
import Visual from "./components/Visual"
import Level from "./components/Level"
import LevelsMarginPadding from "./components/levelvisuals/LevelsMarginPadding"
import LevelsBackground from "./components/levelvisuals/LevelsBackground"
import LevelsBackground2 from "./components/levelvisuals/LevelsBackground2"
import LevelsFlex from "./components/levelvisuals/LevelsFlex"
import LevelsFlexAlignItems from "./components/levelvisuals/LevelsFlexAlignItems"
import LevelsFlexAlignContent from "./components/levelvisuals/LevelsFlexAlignContent"
import LevelsFlexSelf from "./components/levelvisuals/LevelsFlexSelf"
import LevelsFlexWrap1 from "./components/levelvisuals/LevelsFlexWrap1"
import LevelsFlexWrap2 from "./components/levelvisuals/LevelsFlexWrap2"
import LevelsFlexWrap3 from "./components/levelvisuals/LevelsFlexWrap3"
import LevelsFlexGrow from "./components/levelvisuals/LevelsFlexGrow"
import LevelsPosition from "./components/levelvisuals/LevelsPosition"
import LevelsPosition2 from "./components/levelvisuals/LevelsPosition2"
import LevelsTransform from "./components/levelvisuals/LevelsTransform"
import LevelsTransition from "./components/levelvisuals/LevelsTransition"
import LevelsAnimation from "./components/levelvisuals/LevelsAnimation"
export default {
    components: {
        Theory, Coding, Visual, Level,
        //and all the levels visual
        LevelsMarginPadding, LevelsBackground, LevelsBackground2, LevelsFlex, LevelsFlexAlignItems, LevelsFlexAlignContent, LevelsFlexSelf, LevelsFlexWrap1, LevelsFlexWrap2, LevelsFlexWrap3, LevelsFlexGrow, LevelsPosition, LevelsPosition2, LevelsTransform, LevelsTransition, LevelsAnimation
        //and all the levels theory and tasks
        //and all the levels correct answers too
    },
    data(){
        return{
            numbers: [
                {number: 1}, {number: 2}, {number: 3}, {number: 4}, {number: 5}, {number: 6}, {number: 7}, {number: 8}, {number: 9}, {number: 10}],
            levels: [
                {topic: 'margin/padding',  subtopic: [{name: 'margin', levelnumbers: [{num: 1, total: 1}, 
                                                                                      {num: 2, total: 2}, 
                                                                                      {num: 3, total: 3}, 
                                                                                      {num: 4, total: 4}]}, 
                                                      {name: 'padding', levelnumbers: [{num: 1, total: 5}, 
                                                                                       {num: 2, total: 6}, 
                                                                                       {num: 3, total: 7}]}]},

                {topic: 'background', subtopic: [{name: 'color', levelnumbers: [{num: 1, total: 8}, 
                                                                                {num: 2, total: 9}, 
                                                                                {num: 3, total: 10}, 
                                                                                {num: 4, total: 11}]},
                                                 {name: 'gradient', levelnumbers: [{num: 1, total: 12}, 
                                                                                   {num: 2, total: 13}, 
                                                                                   {num: 3, total: 14}, 
                                                                                   {num: 4, total: 15}, 
                                                                                   {num: 5, total: 16}, 
                                                                                   {num: 6, total: 17}, 
                                                                                   {num: 7, total: 18}, 
                                                                                   {num: 8, total: 19}, 
                                                                                   {num: 9, total: 20}, 
                                                                                   {num: 10, total: 21}, 
                                                                                   {num: 11, total: 22}, 
                                                                                   {num: 12, total: 23}, 
                                                                                   {num: 13, total: 24}, 
                                                                                   {num: 14, total: 25}, 
                                                                                   {num: 15, total: 26}]},
                                                 {name: 'image', levelnumbers: [{num: 1, total: 27}, 
                                                                                {num: 2, total: 28}, 
                                                                                {num: 3, total: 29}, 
                                                                                {num: 4, total: 30}, 
                                                                                {num: 5, total: 31}, 
                                                                                {num: 6, total: 32}, 
                                                                                {num: 7, total: 33}, 
                                                                                {num: 8, total: 34}, 
                                                                                {num: 9, total: 35}]}]},
                {topic: 'flex', subtopic: [{name: 'flexdirection', levelnumbers: [{num: 1, total: 36}, 
                                                                                   {num: 2, total: 37}]},
                                           {name: 'justifycontent', levelnumbers: [{num: 1, total: 38}, 
                                                                                   {num: 2, total: 39}, 
                                                                                   {num: 3, total: 40}, 
                                                                                   {num: 4, total: 41}, 
                                                                                   {num: 5, total: 42}]},
                                           {name: 'alignitems', levelnumbers: [{num: 1, total: 43}, 
                                                                               {num: 2, total: 44}, 
                                                                               {num: 3, total: 45}]},
                                           {name: 'aligncontent', levelnumbers: [{num: 1, total: 46}]},
                                           {name: 'alignself', levelnumbers: [{num: 1, total: 47}]},
                                           {name: 'flexwrap', levelnumbers: [{num: 1, total: 48}, 
                                                                             {num: 2, total: 49}, 
                                                                             {num: 3, total: 50}]},
                                           {name: 'flexflow', levelnumbers: [{num: 1, total: 51}]},
                                           {name: 'flexgrow', levelnumbers: [{num: 1, total: 52}]}]},

                {topic: 'position', subtopic: [{name: 'relative', levelnumbers: [{num: 1, total: 53}]},
                                               {name: 'absolute', levelnumbers: [{num: 1, total: 54}]},
                                               {name: 'fixed', levelnumbers: [{num: 1, total: 55}]},
                                               {name: 'sticky', levelnumbers: [{num: 1, total: 56}]}]},
                
                {topic: 'transform', subtopic: [{name: 'rotate', levelnumbers: [{num: 1, total: 57}, 
                                                                                {num: 2, total: 58}]},
                                                {name: 'translate', levelnumbers: [{num: 1, total: 59}, 
                                                                                   {num: 2, total: 60}, 
                                                                                   {num: 3, total: 61}]},
                                                {name: 'scale', levelnumbers: [{num: 1, total: 62}]},
                                                {name: 'skew', levelnumbers: [{num: 1, total: 63}, 
                                                                              {num: 2, total: 64}]},
                                                {name: 'matrix', levelnumbers: [{num: 1, total: 65}, 
                                                                                {num: 2, total: 66}]}]},
                
                {topic: 'transition', subtopic: [{name: 'transitionproperty', levelnumbers: [{num: 1, total: 67}, 
                                                                                             {num: 2, total: 68}, 
                                                                                             {num: 3, total: 69}]},
                                                 {name: 'transitionduration', levelnumbers: [{num: 1, total: 70}]},
                                                 {name: 'transitiontimingfunction', levelnumbers: [{num: 1, total: 71}, 
                                                                                                   {num: 2, total: 72}, 
                                                                                                   {num: 3, total: 73}, 
                                                                                                   {num: 4, total: 74}, 
                                                                                                   {num: 5, total: 75}]},
                                                 {name: 'transitiondelay', levelnumbers: [{num: 1, total: 76}]},
                                                 {name: 'transition', levelnumbers: [{num: 1, total: 77}]}]},
                
                {topic: 'animation', subtopic: [{name: 'animationname', levelnumbers: [{num: 1, total: 78}]},
                                                {name: 'animationduration', levelnumbers: [{num: 1, total: 79}]},
                                                {name: 'animationtimingfunction', levelnumbers: [{num: 1, total: 80}]},
                                                {name: 'animationdelay', levelnumbers: [{num: 1, total: 82}]},
                                                {name: 'animationiterationcount', levelnumbers: [{num: 1, total: 82},
                                                                                                 {num: 2, total: 83}]},
                                                {name: 'animationdirection', levelnumbers: [{num: 1, total: 84},
                                                                                            {num: 2, total: 85},
                                                                                            {num: 3, total: 86}]},
                                                {name: 'animationfillmode', levelnumbers: [{num: 1, total: 87}]},
                                                {name: 'animation', levelnumbers: [{num: 1, total: 88}]}]}    
            ],
            text: '',
            codes: [],
            currentlevel: {topicnumber: 0, topicname: 'margin/padding', subtopicnumber: 0, subtopicname: 'margin', levelinarray: 0, level: 1, totalnumber: 1},
            currentlevelvisual: 'LevelsMarginPadding',
            currentleveltheory: 'Margin1',
            userStyle: '',
            userValue: '',
            correctAnswer: '',
            mainpage: true,
            levelsamount: {current: 0, amount: 0},
            clearArea: false
        }
    },
    methods: {
        checkCss(coding) {
            const newCode = {
                text: coding.text,
                id: coding.id
            }
            if (this.currentlevel.totalnumber == 1)
            {
                if (newCode.text.includes("margin:"))
                {
                    this.userValue = newCode.text.replace("margin:", "")
                    this.userStyle = "--mar: " + this.userValue + " width: calc(50% - var(--mar) * 2); height: calc(50% - var(--mar) * 2); margin: var(--mar);"
                }
            } else if (this.currentlevel.totalnumber == 2)
            {
                this.userValue = newCode.text
                //два значения, так что надо получить первое и второе
                if (this.userValue.includes("margin-bottom") && this.userValue.includes("margin-left"))
                {
                    const margins = this.userValue.split("\n")
                    let mb = ''
                    let ml = ''
                    margins.forEach(st => 
                    {
                        if (st.includes("margin-bottom"))
                        {
                            mb = st.replace("margin-bottom:", "")
                        } else if (st.includes("margin-left"))
                        {
                            ml = st.replace("margin-left:", "")
                        }
                    })
                    this.userStyle = "--mar-l: " + ml + " --mar-b: " + mb + " width: calc(50% - var(--mar-l)); height: calc(50% - var(--mar-b)); margin-bottom: var(--mar-b); margin-left: var(--mar-l);"
                }
            } else if (this.currentlevel.totalnumber == 3)
            {
                if (newCode.text.includes("margin:"))
                {
                    this.userValue = newCode.text.replace("margin:", "")
                    this.userValue = this.userValue.trimStart()
                    //много значений, получить все
                    const margins = this.userValue.split(" ")
                    let mt = margins[0]
                    let mr = margins[1]
                    let mb = margins[2]
                    let ml = margins[3]
                    console.log(margins)
                    let mtnum = mt.replace('px', '')
                    let mrnum = mr.replace('px', '')
                    let mbnum = mb.replace('px', '')
                    let mlnum = ml.replace('px', '')
                    mlnum = mlnum.replace(';', '')
                    let tb = String(Number(mtnum) + Number(mbnum)) + "px"
                    let lr = String(Number(mlnum) + Number(mrnum)) + "px"
                    this.userStyle = "--mar-t: " + mtnum + "px; --mar-r: " + mrnum + "px; --mar-b: " + mbnum + "px; --mar-l: " + mlnum + "px; --tb: " + tb + "; --lr: " + lr + "; width: calc(50% - var(--lr)); height: calc(50% - var(--tb)); margin: var(--mar-t) var(--mar-r) var(--mar-b) var(--mar-l);"               
                }
            } else if (this.currentlevel.totalnumber == 4)
            {
                if (newCode.text.includes("margin:"))
                {
                    this.userValue = newCode.text.replace("margin:", "")
                    this.userValue = this.userValue.trimStart()
                    //два значения, так что надо получить первое и второе
                    const margins = this.userValue.split(" ")
                    let mtb = margins[0]
                    let mlr = margins[1]
                    this.userStyle = "--mar-tb: " + mtb + "; --mar-lr: " + mlr + " width: calc(50% - var(--mar-lr) * 2); height: calc(50% - var(--mar-tb) * 2); margin: var(--mar-tb) var(--mar-lr)"
                }
            } else if (this.currentlevel.totalnumber == 5)
            {
                if (newCode.text.includes("padding:"))
                {
                    this.userValue = newCode.text
                    this.userStyle = this.userValue
                }
            } else if (this.currentlevel.totalnumber == 6)
            {
                this.userValue = newCode.text
                if (this.userValue.includes("padding-bottom") && this.userValue.includes("padding-right"))
                {
                    //два значения, так что надо получить первое и второе
                    const paddings = this.userValue.split("\n")
                    let pb = ''
                    let pr = ''
                    paddings.forEach(st => 
                    {
                        if (st.includes("padding-bottom"))
                        {
                            pb = st.replace("padding-bottom:", "")
                        } else if (st.includes("padding-right"))
                        {
                            pr = st.replace("padding-right:", "")
                        }
                    })
                    this.userStyle = "padding-bottom: " + pb + " padding-right: " + pr
                }
            } else if (this.currentlevel.totalnumber == 7)
            {
                if (newCode.text.includes("padding:"))
                {
                    this.userValue = newCode.text.replace("padding:", "")
                    this.userValue = this.userValue.trimStart()
                    //много значений, получить все
                    const paddings = this.userValue.split(" ")
                    let pt = paddings[0]
                    let plr = paddings[1]
                    let pb = paddings[2]
                    this.userStyle = "padding: " + pt + " " + plr + " " + pb + ";"
                }
            } else if (this.currentlevel.totalnumber == 8)
            {
                if (newCode.text.includes("background-color:"))
                {
                    this.userValue = newCode.text
                    this.userStyle = this.userValue
                }
            } else if (this.currentlevel.totalnumber == 9)
            {
                if (newCode.text.includes("background-color:") && newCode.text.includes("#"))
                {
                    this.userValue = newCode.text
                    this.userStyle = this.userValue
                }
            } else if (this.currentlevel.totalnumber == 10)
            {
                if (newCode.text.includes("background-color:") && newCode.text.includes("rgba"))
                {
                    this.userValue = newCode.text
                    this.userStyle = this.userValue
                }
            } else if (this.currentlevel.totalnumber == 11)
            {
                if (newCode.text.includes("background-color:") && newCode.text.includes("hsla"))
                {
                    this.userValue = newCode.text
                    this.userStyle = this.userValue
                }
            } else if (this.currentlevel.totalnumber == 12 || this.currentlevel.totalnumber == 13 || this.currentlevel.totalnumber == 14)
            {
                if (newCode.text.includes("background:") && newCode.text.includes("linear-gradient"))
                {
                    this.userValue = newCode.text
                    this.userStyle = this.userValue
                }
            } else if (this.currentlevel.totalnumber == 15 || this.currentlevel.totalnumber == 16)
            {
                if (newCode.text.includes("background:") && newCode.text.includes("radial-gradient"))
                {
                    this.userValue = newCode.text
                    this.userStyle = this.userValue
                }
            } else if (this.currentlevel.totalnumber >= 17 && this.currentlevel.totalnumber <= 19)
            {
                if (newCode.text.includes("background:") && newCode.text.includes("conic-gradient"))
                {
                    this.userValue = newCode.text
                    this.userStyle = this.userValue
                }
            } else if (this.currentlevel.totalnumber >= 20 && this.currentlevel.totalnumber <= 23)
            {
                if (newCode.text.includes("background:") && newCode.text.includes("repeating-linear-gradient"))
                {
                    this.userValue = newCode.text
                    this.userStyle = this.userValue
                }
            } else if (this.currentlevel.totalnumber == 24)
            {
                if (newCode.text.includes("background:") && newCode.text.includes("repeating-radial-gradient"))
                {
                    this.userValue = newCode.text
                    this.userStyle = this.userValue
                }
            } else if (this.currentlevel.totalnumber == 25)
            {
                if (newCode.text.includes("background:") && newCode.text.includes("radial-gradient"))
                {
                    this.userValue = newCode.text
                    this.userStyle = this.userValue
                }
            } else if (this.currentlevel.totalnumber == 26)
            {
                if (newCode.text.includes("background:") && newCode.text.includes("linear-gradient"))
                {
                    this.userValue = newCode.text
                    this.userStyle = this.userValue
                }
            } else if (this.currentlevel.totalnumber >= 27 && this.currentlevel.totalnumber <= 30)
            {
                if (newCode.text.includes("background-repeat:"))
                {
                    this.userValue = newCode.text
                    this.userStyle = this.userValue
                }
            } else if (this.currentlevel.totalnumber == 31 || this.currentlevel.totalnumber == 32)
            {
                if (newCode.text.includes("background-position:"))
                {
                    this.userValue = newCode.text
                    this.userStyle = this.userValue
                }
            } else if (this.currentlevel.totalnumber >= 33 && this.currentlevel.totalnumber <= 35)
            {
                if (newCode.text.includes("background-size:"))
                {
                    this.userValue = newCode.text
                    this.userStyle = this.userValue
                }
            } else if (this.currentlevel.totalnumber == 36 || this.currentlevel.totalnumber == 37)
            {
                console.log('check')
                if (newCode.text.includes("display: flex;"))
                {
                    this.userValue = newCode.text
                    this.userStyle = this.userValue
                }
            } else if (this.currentlevel.totalnumber >= 38 && this.currentlevel.totalnumber <= 42)
            {
                // if (newCode.text.includes("display: flex;") && newCode.text.includes("justify-content:"))
                if (newCode.text.includes("display: flex;"))
                {
                    this.userValue = newCode.text
                    this.userStyle = this.userValue
                }
            } else if (this.currentlevel.totalnumber >= 43 && this.currentlevel.totalnumber <= 45)
            {
                // if (newCode.text.includes("display: flex;") && newCode.text.includes("align-items:"))
                if (newCode.text.includes("display: flex;"))

                {
                    this.userValue = newCode.text
                    this.userStyle = this.userValue
                }
            } else if (this.currentlevel.totalnumber == 46)
            {
                // if (newCode.text.includes("display: flex;") && newCode.text.includes("align-content:"))
                if (newCode.text.includes("display: flex;"))
                {
                    this.userValue = newCode.text
                    this.userStyle = this.userValue
                }
            } else if (this.currentlevel.totalnumber == 47)
            {
                // if (newCode.text.includes("display: flex;") && newCode.text.includes("align-self:"))
                if (newCode.text.includes("align-self"))
                {
                    this.userValue = newCode.text
                    this.userStyle = this.userValue
                }
            } else if (this.currentlevel.totalnumber >= 48 && this.currentlevel.totalnumber <= 50)
            {
                // if (newCode.text.includes("display: flex;") && newCode.text.includes("flex-wrap:"))
                if (newCode.text.includes("display: flex;"))
                {
                    this.userValue = newCode.text
                    this.userStyle = this.userValue
                }
            } else if (this.currentlevel.totalnumber == 51)
            {
                // if (newCode.text.includes("display: flex;") && newCode.text.includes("flex-flow:"))
                if (newCode.text.includes("display: flex;"))
                {
                    this.userValue = newCode.text
                    this.userStyle = this.userValue
                }
            } else if (this.currentlevel.totalnumber == 52)
            {
                // if (newCode.text.includes("display: flex;") && newCode.text.includes("flex-grow:"))
                if (newCode.text.includes("display: flex;"))
                {
                    this.userValue = newCode.text
                    this.userStyle = this.userValue
                }
            } else if (this.currentlevel.totalnumber == 53)
            {
                if (newCode.text.includes("position: relative;"))
                {
                    this.userValue = newCode.text
                    this.userStyle = this.userValue
                }
            } else if (this.currentlevel.totalnumber == 54)
            {
                if (newCode.text.includes("position: absolute;"))
                {
                    this.userValue = newCode.text
                    this.userStyle = this.userValue
                }
            } else if (this.currentlevel.totalnumber == 55)
            {
                if (newCode.text.includes("position: fixed;"))
                {
                    this.userValue = newCode.text
                    this.userStyle = this.userValue
                }
            } else if (this.currentlevel.totalnumber == 56)
            {
                if (newCode.text.includes("position: sticky;"))
                {
                    this.userValue = newCode.text
                    this.userStyle = this.userValue
                }
            } else if (this.currentlevel.totalnumber == 57 || this.currentlevel.totalnumber == 58)
            {
                if (newCode.text.includes("transform: rotate"))
                {
                    this.userValue = newCode.text
                    this.userStyle = this.userValue
                }
            } else if (this.currentlevel.totalnumber == 59)
            {
                if (newCode.text.includes("transform: translate"))
                {
                    this.userValue = newCode.text
                    this.userStyle = this.userValue
                }
            } else if (this.currentlevel.totalnumber == 60 || this.currentlevel.totalnumber == 61)
            {
                if (newCode.text.includes("transform:") && newCode.text.includes("rotate") && newCode.text.includes("translate"))
                {
                    this.userValue = newCode.text
                    this.userStyle = this.userValue
                }
            } else if (this.currentlevel.totalnumber == 62)
            {
                if (newCode.text.includes("transform: scale"))
                {
                    this.userValue = newCode.text
                    this.userStyle = this.userValue
                }
            } else if (this.currentlevel.totalnumber == 63 || this.currentlevel.totalnumber == 64)
            {
                if (newCode.text.includes("transform: skew"))
                {
                    this.userValue = newCode.text
                    this.userStyle = this.userValue
                }
            } else if (this.currentlevel.totalnumber == 65 || this.currentlevel.totalnumber == 66)
            {
                if (newCode.text.includes("transform: matrix"))
                {
                    this.userValue = newCode.text
                    this.userStyle = this.userValue
                }
            } else if (this.currentlevel.totalnumber >= 67 && this.currentlevel.totalnumber <= 69)
            {
                if (newCode.text.includes("transition-property:"))
                {
                    this.userValue = newCode.text
                    this.userStyle = this.userValue
                }
            } else if (this.currentlevel.totalnumber == 70)
            {
                if (newCode.text.includes("transition-duration:"))
                {
                    this.userValue = newCode.text
                    this.userStyle = this.userValue
                }
            } else if (this.currentlevel.totalnumber >= 71 && this.currentlevel.totalnumber <= 75)
            {
                if (newCode.text.includes("transition-timing-function:"))
                {
                    this.userValue = newCode.text
                    this.userStyle = this.userValue
                }
            } else if (this.currentlevel.totalnumber == 76)
            {
                if (newCode.text.includes("transition-delay:"))
                {
                    this.userValue = newCode.text
                    this.userStyle = this.userValue
                }
            } else if (this.currentlevel.totalnumber == 77)
            {
                if (newCode.text.includes("transition:"))
                {
                    this.userValue = newCode.text
                    this.userStyle = this.userValue
                }
            } else if (this.currentlevel.totalnumber == 78)
            {
                if (newCode.text.includes("animation-name:"))
                {
                    this.userValue = newCode.text
                    this.userStyle = this.userValue
                }
            } else if (this.currentlevel.totalnumber == 79)
            {
                if (newCode.text.includes("animation-duration:"))
                {
                    this.userValue = newCode.text
                    this.userStyle = this.userValue
                }
            } else if (this.currentlevel.totalnumber == 80)
            {
                if (newCode.text.includes("animation-timing-function:"))
                {
                    this.userValue = newCode.text
                    this.userStyle = this.userValue
                }
            } else if (this.currentlevel.totalnumber == 81)
            {
                if (newCode.text.includes("animation-delay:"))
                {
                    this.userValue = newCode.text
                    this.userStyle = this.userValue
                }
            } else if (this.currentlevel.totalnumber == 82 || this.currentlevel.totalnumber == 83)
            {
                if (newCode.text.includes("animation-iteration-count:"))
                {
                    this.userValue = newCode.text
                    this.userStyle = this.userValue
                }
            } else if (this.currentlevel.totalnumber == 84 || this.currentlevel.totalnumber == 86)
            {
                if (newCode.text.includes("animation-direction:"))
                {
                    this.userValue = newCode.text
                    this.userStyle = this.userValue
                }
            } else if (this.currentlevel.totalnumber == 87)
            {
                if (newCode.text.includes("animation-fill-mode:"))
                {
                    this.userValue = newCode.text
                    this.userStyle = this.userValue
                }
            } else if (this.currentlevel.totalnumber == 88)
            {
                if (newCode.text.includes("animation:"))
                {
                    this.userValue = newCode.text
                    this.userStyle = this.userValue
                }
            }
            this.codes.push(newCode)
        },
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
            this.currentlevel = newLevel
            this.userStyle = ''
            this.userValue = ''
            let current = 0
            if (this.currentlevel.subtopicnumber != 0) {
                for (let i = 0; i < this.currentlevel.subtopicnumber; i++)
                {
                    current += this.levels[this.currentlevel.topicnumber].subtopic[i].levelnumbers.length
                }
                current += this.currentlevel.level
            } else {current = this.currentlevel.level}
            let count = 0
            this.levels[this.currentlevel.topicnumber].subtopic.forEach(sub => {
                count += sub.levelnumbers.length
            });
            this.levelsamount.current = current
            this.levelsamount.amount = count
            document.getElementById('typehere').value = ''
        },
        changevisual(visualname) {
            const newvisual = visualname
            this.currentlevelvisual = newvisual
        },
        changetheory(theoryname) {
            const newtheory = theoryname
            this.currentleveltheory = newtheory
        },
        chooseTopic(event) {
            const number = event.target.innerHTML.charAt(0)-1
            const newLevel = {
                topicnumber: number, 
                topicname: this.levels[number].topic, 
                subtopicnumber: 0,
                subtopicname: this.levels[number].subtopic[0].name,
                levelinarray: 0, 
                level: 1,
                totalnumber: this.levels[number].subtopic[0].levelnumbers[0].total
            }
            const newVisual = this.getVisual(newLevel.totalnumber)
            const newTheory = newLevel.subtopicname + 1
            this.currentlevel = newLevel
            this.currentlevelvisual = newVisual
            this.currentleveltheory = newTheory
            const newLevelsAmount = this.getLevelsAmount()
            this.levelsamount = newLevelsAmount
            this.mainpage = false
            // вызывать ещё как-то смену визуала и смену теории здесь
        },
        backToMain() {
            this.mainpage = true
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
            } else if (levelnumber == 48 || levelnumber == 51) {
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
            }  else if (levelnumber >= 57 && levelnumber <= 66) {
                levelvisualname = 'LevelsTransform'
            } else if (levelnumber >= 67 && levelnumber <= 77) {
                levelvisualname = 'LevelsTransition'
            } else if (levelnumber >= 78 && levelnumber <= 88) {
                levelvisualname = 'LevelsAnimation'
            }
            return levelvisualname
        },
        getLevelsAmount() {
            let count = 0
            this.levels[this.currentlevel.topicnumber].subtopic.forEach(sub => {
                count += sub.levelnumbers.length
            });
            let current = 0
            if (this.currentlevel.subtopicnumber != 0) {
                for (let i = 0; i < this.currentlevel.subtopicnumber; i++)
                {
                    current += this.levels[this.currentlevel.topicnumber].subtopic[i].levelnumbers.length
                }
                current += this.currentlevel.level
            } else {current = this.currentlevel.level}
            const newLevelsAmount = {current: current, amount: count}
            return newLevelsAmount
        },
        clearTextbox() {
            this.clearArea = true
            document.getElementById('showAnswer').style="visibility: hidden;"
            document.getElementById('nextlvl').style="visibility: hidden;"
        },
        unclear() {
            this.clearArea = false
        }
    } 
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Fredoka+One&display=swap');
*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: "Century Gothic", CenturyGothic, AppleGothic, sans-serif;
}
.application{
    display: flex;
    justify-content: space-around;
    width: 100%;
    height: 100vh;
    background-color: rgb(255, 200, 0);
}
.left{
    display: flex;
    flex-direction: column;
    width: calc(55% - 80px);
    margin: 40px;
    height: calc(100% - 80px);
    justify-content: space-between;
}

.right{
    width: calc(45% - 40px);
    margin: 40px 40px 40px 0px;
    height: calc(100% - 80px);
}
.topic-item{
    display: flex;
    width: 20%;
    height: 40%;
    background: red;
    margin: 2% 2.5%;
    border-radius: 10%;
    justify-content: center;
    align-items: center;
    text-transform: lowercase;
    text-align: center;
    font-size: 24px;

}
.main ul{
    display: flex;
    flex-direction: row;
    list-style-type: none;
    flex-wrap: wrap;
    justify-content: center;
    height: 60%;
    align-items: center;
    align-content: center;
    margin: 0 10%;
}
.main{
    width: 100%;
    height: 100vh;
}
.header{
    text-transform: uppercase;
    font-size: 92px;
    text-align: center;
    height: 30%;
    padding-top: 5%;
    font-family: 'Fredoka One', cursive;
}
.item1{
    background: url("C:\Users\malah\Desktop\Документы\lena\css_schowl\public\mp.png") center/cover no-repeat;
}
.item2{
    background: url("C:\Users\malah\Desktop\Документы\lena\css_schowl\public\bg.png") center/cover no-repeat;
}
.item3{
    background: url("C:\Users\malah\Desktop\Документы\lena\css_schowl\public\flex.png") center/cover no-repeat;
}
.item4{
    background: url("C:\Users\malah\Desktop\Документы\lena\css_schowl\public\pos.png") center/cover no-repeat;
}
.item5{
    background: url("C:\Users\malah\Desktop\Документы\lena\css_schowl\public\transform.png") center/cover no-repeat;
}
.item6{
    background: url("C:\Users\malah\Desktop\Документы\lena\css_schowl\public\transition.png") center/cover no-repeat;
}
.item7{
    background: url("C:\Users\malah\Desktop\Документы\lena\css_schowl\public\anim.png") center/cover no-repeat;
}
.back-btn{
    color: black;
    font-size: 20px;
    width: fit-content;
    padding: 10px;
    position: absolute;
    top: 10px;
    left: 10px;
    border: none;
    font-weight: bold;
    display: flex;
    align-items: center;
    background-color: rgb(255, 180, 0);
    border-radius: 10px;
}
.back-btn img{
    width: 25px;
}
.levelpage{
    display: flex;
    justify-content: space-around;
    width: 100%;
    height: 100vh;
    background-color: rgb(255, 200, 0);
}

</style>