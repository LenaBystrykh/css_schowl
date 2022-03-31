<template>
    <div class="coding">
        <div class="code-place">
            <div class="stringnumbers">
                <div class="nums" v-for="num in numbers">
                    <div>{{ num.number }}</div>
                </div>
            </div>
            <!-- <textarea v-bind:value="coding.text" @input="coding.text = $event.target.value" class="typehere" placeholder="Type your code here"></textarea> -->
            <textarea v-model="coding.text" id="typehere" placeholder="Type your code here"></textarea>
        </div>
        <div class="buttons">
            <button class="check" @click="checkCss">Проверить!</button>
            <button class="showAnswer" id="showAnswer" @click="showCorrectAnswer">Посмотреть ответ</button>
            <button class="nextlvl" id="nextlvl" @click="goNext">Далее</button>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        levels: {
            type: Array,
            required: true
        },
        numbers: {
            type: Array,
            required: true
        },
        codes: {
            type: Array,
            required: true
        },
        correctAnswer: {
            type: String,
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
        clearArea: {
            type: Boolean,
            required: true
        }
    },
    data() {
        return {
            coding: {
                text: ''
            },
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
            needHelp: false
        }
    },
    methods: {
        checkCss() {
            //event.preventDefault()
            // в скобочках у чекссс ивент
            if (this.currentlevel.totalnumber == 1)
            {
                let answ = this.correctAnswer
                answ ='margin: 20px;'
                this.checkAnswer(answ)
            } else if (this.currentlevel.totalnumber == 2)
            {
                let answ = this.correctAnswer
                answ = 'margin-left: 15px;\nmargin-bottom: 50px;ORmargin-bottom: 50px;\nmargin-left: 15px;'
                answ = answ.split("OR")
                answ.forEach(answer => {
                    this.checkAnswer(answer)
                })
            } else if (this.currentlevel.totalnumber == 3)
            {
                let answ = this.correctAnswer
                answ = 'margin: 15px 30px 30px 0;ORmargin: 15px 30px 30px 0px;'
                answ = answ.split("OR")
                answ.forEach(answer => {
                    this.checkAnswer(answer)
                })
            } else if (this.currentlevel.totalnumber == 4)
            {
                let answ = this.correctAnswer
                answ = 'margin: 10px 30px;'
                this.checkAnswer(answ)
            } else if (this.currentlevel.totalnumber == 5)
            {
                let answ = this.correctAnswer
                answ = 'padding: 10px;'
                this.checkAnswer(answ)
            } else if (this.currentlevel.totalnumber == 6)
            {
                let answ = this.correctAnswer
                answ = 'padding-bottom: 20px;\npadding-right: 10px;ORpadding-right: 10px;\npadding-bottom: 20px;'
                answ = answ.split("OR")
                answ.forEach(answer => {
                    this.checkAnswer(answer)
                })
            } else if (this.currentlevel.totalnumber == 7)
            {
                let answ = this.correctAnswer
                answ = 'padding: 50px 15px 5px;'
                this.checkAnswer(answ)
            } else if (this.currentlevel.totalnumber == 8)
            {
                let answ = this.correctAnswer
                answ = 'background-color: green;'
                this.checkAnswer(answ)
            } else if (this.currentlevel.totalnumber == 9)
            {
                let answ = this.correctAnswer
                answ = 'background-color: #8F89FF;'
                this.checkAnswer(answ)
            } else if (this.currentlevel.totalnumber == 10)
            {
                let answ = this.correctAnswer
                answ = 'background-color: rgba(190, 255, 130, 0.7);'
                this.checkAnswer(answ)
            } else if (this.currentlevel.totalnumber == 11)
            {
                let answ = this.correctAnswer
                answ = 'background-color: hsla(300, 15%, 90%, 0.3);'
                this.checkAnswer(answ)
            } else if (this.currentlevel.totalnumber == 12)
            {
                let answ = this.correctAnswer
                answ = 'background: linear-gradient(45deg, #B460FF, #AD84FF, #4D7DFF, #4DE4FF);'
                this.checkAnswer(answ)
            } else if (this.currentlevel.totalnumber == 13)
            {
                let answ = this.correctAnswer
                answ = 'background: linear-gradient(45deg, #B460FF 40%, #AD84FF 55%, #4D7DFF 65%, #4DE4FF 100%);ORbackground: linear-gradient(45deg, #B460FF 40%, #AD84FF 55%, #4D7DFF 65%, #4DE4FF);'
                answ = answ.split("OR")
                answ.forEach(answer => {
                    this.checkAnswer(answer)
                })
            } else if (this.currentlevel.totalnumber == 14)
            {
                let answ = this.correctAnswer
                answ = 'background: linear-gradient(30deg, red 15%, yellow 75% 90%, pink 90%);ORbackground: linear-gradient(30deg, red 0% 15%, yellow 75% 90%, pink 90% 100%);ORbackground: linear-gradient(30deg, red 0% 15%, yellow 75% 90%, pink 90%);ORbackground: linear-gradient(30deg, red 15%, yellow 75% 90%, pink 90% 100%);'
                answ = answ.split("OR")
                answ.forEach(answer => {
                    this.checkAnswer(answer)
                })
            } else if (this.currentlevel.totalnumber == 15)
            {
                let answ = this.correctAnswer
                answ = 'background: radial-gradient(lightblue 100px, violet 50%, magenta 70%);'
                this.checkAnswer(answ)
            } else if (this.currentlevel.totalnumber == 16)
            {
                let answ = this.correctAnswer
                answ = 'background: radial-gradient(at 20px 25%, orange 40%, red 60%);'
                this.checkAnswer(answ)
            } else if (this.currentlevel.totalnumber == 17)
            {
                let answ = this.correctAnswer
                answ = 'background: conic-gradient(#4D52FF, #FFFFFF, #8B18E5);'
                this.checkAnswer(answ)
            } else if (this.currentlevel.totalnumber == 18)
            {
                let answ = this.correctAnswer
                answ = 'background: conic-gradient(at 30% 70%, #4D52FF 30%, #FFFFFF 60%, #8B18E5 80%);'
                this.checkAnswer(answ)
            } else if (this.currentlevel.totalnumber == 19)
            {
                let answ = this.correctAnswer
                answ = 'background: conic-gradient(from 120deg, #4D52FF, #FFFFFF, #8B18E5);'
                this.checkAnswer(answ)
            } else if (this.currentlevel.totalnumber == 20)
            {
                let answ = this.correctAnswer
                answ = 'background: repeating-linear-gradient(60deg, red 10px, red 20px, pink 40px, pink 80px);'
                this.checkAnswer(answ)
            } else if (this.currentlevel.totalnumber == 21)
            {
                let answ = this.correctAnswer
                answ = 'background: repeating-linear-gradient(45deg, orange, pink 10%);'
                this.checkAnswer(answ)
            } else if (this.currentlevel.totalnumber == 22)
            {
                let answ = this.correctAnswer
                answ = 'background: repeating-linear-gradient(to left, pink, white, red 250px);'
                this.checkAnswer(answ)
            } else if (this.currentlevel.totalnumber == 23)
            {
                let answ = this.correctAnswer
                answ = 'background: repeating-linear-gradient(to top right, #4D52FF 0%, #FFFFFF 10%, #8B18E5 20%);'
                this.checkAnswer(answ)
            } else if (this.currentlevel.totalnumber == 24)
            {
                let answ = this.correctAnswer
                answ = 'background: repeating-radial-gradient(red 0px, red 50px, pink 50px, pink 100px);'
                this.checkAnswer(answ)
            } else if (this.currentlevel.totalnumber == 25)
            {
                let answ = this.correctAnswer
                answ = 'background: radial-gradient(circle at 50% 0, rgba(255, 0, 0, 0.5), rgba(255, 0, 0, 0) 75%), radial-gradient(circle at 5% 75%, rgba(0, 0, 255, 0.5), rgba(0, 0, 255, 0) 75%), radial-gradient(circle at 95% 75%, rgba(0, 255, 0, 0.5), rgba(0, 255, 0, 0) 75%) beige;'
                this.checkAnswer(answ)
            } else if (this.currentlevel.totalnumber == 26)
            {
                let answ = this.correctAnswer
                answ = 'background: linear-gradient(90deg, rgba(255, 255, 0, 0.5), rgba(255, 150, 0, 0.5), rgba(255, 170, 230, 0.5)), url("https://cdn-icons-png.flaticon.com/512/1864/1864652.png") center/cover no-repeat;'
                this.checkAnswer(answ)
            } else if (this.currentlevel.totalnumber == 27)
            {
                let answ = this.correctAnswer
                answ = 'background-repeat: repeat-x;'
                this.checkAnswer(answ)
            } else if (this.currentlevel.totalnumber == 28)
            {
                let answ = this.correctAnswer
                answ = 'background-repeat: repeat;'
                this.checkAnswer(answ)
            } else if (this.currentlevel.totalnumber == 29)
            {
                let answ = this.correctAnswer
                answ = 'background-repeat: space;'
                this.checkAnswer(answ)
            } else if (this.currentlevel.totalnumber == 30)
            {
                let answ = this.correctAnswer
                answ = 'background-repeat: round;'
                this.checkAnswer(answ)
            } else if (this.currentlevel.totalnumber == 31)
            {
                let answ = this.correctAnswer
                answ = 'background-position: 50px 60%;'
                this.checkAnswer(answ)
            } else if (this.currentlevel.totalnumber == 32)
            {
                let answ = this.correctAnswer
                answ = 'background-repeat: repeat-x;\nbackground-position: left bottom;ORbackground-position: left bottom;\nbackground-repeat: repeat-x;'
                answ = answ.split("OR")
                answ.forEach(answer => {
                    this.checkAnswer(answer)
                })
            } else if (this.currentlevel.totalnumber == 33)
            {
                let answ = this.correctAnswer
                answ = 'background-size: 500px 500px;'
                this.checkAnswer(answ)
            } else if (this.currentlevel.totalnumber == 34)
            {
                let answ = this.correctAnswer
                answ = 'background-size: contain;'
                this.checkAnswer(answ)
            } else if (this.currentlevel.totalnumber == 35)
            {
                let answ = this.correctAnswer
                answ = 'background-size: cover;'
                this.checkAnswer(answ)
            } else if (this.currentlevel.totalnumber == 36)
            {
                let answ = this.correctAnswer
                answ = 'display: flex;\nflex-direction: row-reverse;'
                this.checkAnswer(answ)
            } else if (this.currentlevel.totalnumber == 37)
            {
                let answ = this.correctAnswer
                answ = 'display: flex;\nflex-direction: column;'
                this.checkAnswer(answ)
            } else if (this.currentlevel.totalnumber == 38)
            {
                let answ = this.correctAnswer
                answ = 'display: flex;\njustify-content: flex-start;ORdisplay: flex;\nflex-direction: row;\njustify-content: flex-start;ORdisplay: flex;\njustify-content: flex-start;\nflex-direction: row;'
                answ = answ.split("OR")
                answ.forEach(answer => {
                    this.checkAnswer(answer)
                })
            } else if (this.currentlevel.totalnumber == 39)
            {
                let answ = this.correctAnswer
                answ = 'display: flex;\nflex-direction: column;\njustify-content: center;ORdisplay: flex;\njustify-content: center;\nflex-direction: column;'
                answ = answ.split("OR")
                answ.forEach(answer => {
                    this.checkAnswer(answer)
                })
            } else if (this.currentlevel.totalnumber == 40)
            {
                let answ = this.correctAnswer
                answ = 'display: flex;\njustify-content: space-between;'
                this.checkAnswer(answ)
            } else if (this.currentlevel.totalnumber == 41)
            {
                let answ = this.correctAnswer
                answ = 'display: flex;\njustify-content: space-around;'
                this.checkAnswer(answ)
            } else if (this.currentlevel.totalnumber == 42)
            {
                let answ = this.correctAnswer
                answ = 'display: flex;\nflex-direction: column-reverse;\njustify-content: space-evenly;ORdisplay: flex;\njustify-content: space-evenly;\nflex-direction: column-reverse;'
                answ = answ.split("OR")
                answ.forEach(answer => {
                    this.checkAnswer(answer)
                })
            } else if (this.currentlevel.totalnumber == 43)
            {
                let answ = this.correctAnswer
                answ = 'display: flex;\njustify-content: center;\nalign-items: center;ORdisplay: flex;\nalign-items: center;\njustify-content: center;'
                answ = answ.split("OR")
                answ.forEach(answer => {
                    this.checkAnswer(answer)
                })
            } else if (this.currentlevel.totalnumber == 44)
            {
                let answ = this.correctAnswer
                answ = 'display: flex;\nalign-items: baseline;ORdisplay: flex;\nalign-items: baseline;\nflex-direction: row;ORdisplay: flex;\nflex-direction: row;\nalign-items: baseline;'
                answ = answ.split("OR")
                answ.forEach(answer => {
                    this.checkAnswer(answer)
                })
            } else if (this.currentlevel.totalnumber == 45)
            {
                let answ = this.correctAnswer
                answ = 'display: flex;\nalign-items: stretch;\nflex-direction: row;ORdisplay: flex;\nflex-direction: row;\nalign-items: stretch;'
                answ = answ.split("OR")
                answ.forEach(answer => {
                    this.checkAnswer(answer)
                })
            } else if (this.currentlevel.totalnumber == 46)
            {
                let answ = this.correctAnswer
                answ = 'display: flex;\nalign-content: center;'
                this.checkAnswer(answ)
            } else if (this.currentlevel.totalnumber == 47)
            {
                let answ = this.correctAnswer
                answ = 'align-self: flex-start;'
                this.checkAnswer(answ)
            } else if (this.currentlevel.totalnumber == 48)
            {
                let answ = this.correctAnswer
                answ = 'display: flex;\nflex-wrap: nowrap;'
                this.checkAnswer(answ)
            } else if (this.currentlevel.totalnumber == 49)
            {
                let answ = this.correctAnswer
                answ = 'display: flex;\nflex-wrap: wrap;'
                this.checkAnswer(answ)
            } else if (this.currentlevel.totalnumber == 50)
            {
                let answ = this.correctAnswer
                answ = 'display: flex;\nflex-wrap: wrap-reverse;'
                this.checkAnswer(answ)
            } else if (this.currentlevel.totalnumber == 51)
            {
                let answ = this.correctAnswer
                answ = 'display: flex;\nflex-flow: row-reverse nowrap;'
                this.checkAnswer(answ)
            } else if (this.currentlevel.totalnumber == 52)
            {
                let answ = this.correctAnswer
                answ = 'display: flex;\nflex-grow: 1;'
                this.checkAnswer(answ)
            } else if (this.currentlevel.totalnumber == 53)
            {
                let answ = this.correctAnswer
                answ = 'position: relative;\nbottom: 50px;\nright: 30px;ORposition: relative;\nright: 30px;\nbottom: 50px;ORposition: relative;\ntop: -50px;\nleft: -30px;ORposition: relative;\nleft: -30px;\ntop: -50px;ORposition: relative;\nbottom: 50px;\nleft: -30px;ORposition: relative;\nleft: -30px;\nbottom: 50px;ORposition: relative;\ntop: -50px;\nright: 30px;ORposition: relative;\nright: 30px;\ntop: -50px;'
                answ = answ.split("OR")
                answ.forEach(answer => {
                    this.checkAnswer(answer)
                })
            } else if (this.currentlevel.totalnumber == 54)
            {
                let answ = this.correctAnswer
                answ = 'position: absolute;\ntop: 50px;\nleft: 30px;ORposition: absolute;\nleft: 30px;\ntop: 50px;'
                answ = answ.split("OR")
                answ.forEach(answer => {
                    this.checkAnswer(answer)
                })
            } else if (this.currentlevel.totalnumber == 55)
            {
                let answ = this.correctAnswer
                answ = 'position: fixed;\nbottom: 50px;\nright: 50px;ORposition: fixed;\nright: 50px;\nbottom: 50px;'
                answ = answ.split("OR")
                answ.forEach(answer => {
                    this.checkAnswer(answer)
                })
            } else if (this.currentlevel.totalnumber == 56)
            {
                let answ = this.correctAnswer
                answ = 'position: sticky;\ntop: 20px;'
                this.checkAnswer(answ)
            } else if (this.currentlevel.totalnumber == 57)
            {
                let answ = this.correctAnswer
                answ = 'transform: rotate(70deg);'
                this.checkAnswer(answ)
            } else if (this.currentlevel.totalnumber == 58)
            {
                let answ = this.correctAnswer
                answ = 'transform: rotate(0.5turn);'
                this.checkAnswer(answ)
            } else if (this.currentlevel.totalnumber == 59)
            {
                let answ = this.correctAnswer
                answ = 'transform: translate(-50px, -40%);'
                this.checkAnswer(answ)
            } else if (this.currentlevel.totalnumber == 60)
            {
                let answ = this.correctAnswer
                answ = 'transform: translate(100px, 30px) rotate(90deg);'
                this.checkAnswer(answ)
            } else if (this.currentlevel.totalnumber == 61)
            {
                let answ = this.correctAnswer
                answ = 'transform: rotate(90deg) translate(100px, 30px);'
                this.checkAnswer(answ)
            } else if (this.currentlevel.totalnumber == 62)
            {
                let answ = this.correctAnswer
                answ = 'transform: scale(0.5, 2);'
                this.checkAnswer(answ)
            } else if (this.currentlevel.totalnumber == 63)
            {
                let answ = this.correctAnswer
                answ = 'transform: skewX(-30deg);'
                this.checkAnswer(answ)
            } else if (this.currentlevel.totalnumber == 64)
            {
                let answ = this.correctAnswer
                answ = 'transform: skew(10deg, 10deg);'
                this.checkAnswer(answ)
            } else if (this.currentlevel.totalnumber == 65)
            {
                let answ = this.correctAnswer
                answ = 'transform: matrix(1.2, 0, 1.5, 2, 70, -50);'
                this.checkAnswer(answ)
            } else if (this.currentlevel.totalnumber == 66)
            {
                let answ = this.correctAnswer
                answ = 'transform: matrix(0.5, -0.5, -0.2, 1.5, 10, 20);'
                this.checkAnswer(answ)
            } else if (this.currentlevel.totalnumber == 67)
            {
                let answ = this.correctAnswer
                answ = 'transition-property: background-color;'
                this.checkAnswer(answ)
            } else if (this.currentlevel.totalnumber == 68)
            {
                let answ = this.correctAnswer
                answ = 'transition-property: none;'
                this.checkAnswer(answ)
            } else if (this.currentlevel.totalnumber == 69)
            {
                let answ = this.correctAnswer
                answ = 'transition-property: all;'
                this.checkAnswer(answ)
            } else if (this.currentlevel.totalnumber == 70)
            {
                let answ = this.correctAnswer
                answ = 'transition-duration: 4s;'
                this.checkAnswer(answ)
            } else if (this.currentlevel.totalnumber == 71)
            {
                let answ = this.correctAnswer
                answ = 'transition-timing-function: ease-in;'
                this.checkAnswer(answ)
            } else if (this.currentlevel.totalnumber == 72)
            {
                let answ = this.correctAnswer
                answ = 'transition-timing-function: step-start;'
                this.checkAnswer(answ)
            } else if (this.currentlevel.totalnumber == 73)
            {
                let answ = this.correctAnswer
                answ = 'transition-timing-function: cubic-bezier(0.1, 0.45, 0.9, 0.55);'
                this.checkAnswer(answ)
            } else if (this.currentlevel.totalnumber == 74)
            {
                let answ = this.correctAnswer
                answ = 'transition-timing-function: steps(5, jump-end);'
                this.checkAnswer(answ)
            } else if (this.currentlevel.totalnumber == 75)
            {
                let answ = this.correctAnswer
                answ = 'transition-timing-function: steps(5, jump-both);'
                this.checkAnswer(answ)
            } else if (this.currentlevel.totalnumber == 76)
            {
                let answ = this.correctAnswer
                answ = 'transition-delay: 3s;'
                this.checkAnswer(answ)
            } else if (this.currentlevel.totalnumber == 77)
            {
                let answ = this.correctAnswer
                answ = 'transition: width, 3s, steps(4, jump-start), 0.5s;'
                this.checkAnswer(answ)
            } else if (this.currentlevel.totalnumber == 78)
            {
                let answ = this.correctAnswer
                answ = 'animation-name: fly;'
                this.checkAnswer(answ)
            } else if (this.currentlevel.totalnumber == 79)
            {
                let answ = this.correctAnswer
                answ = 'animation-duration: 5s;\nanimation-name: fly;ORanimation-name: fly;\nanimation-duration: 5s;ORanimation-name: isparenie;\nanimation-duration: 5s;ORanimation-duration: 5s;\nanimation-name: ispareine;'
                answ = answ.split("OR")
                answ.forEach(answer => {
                    this.checkAnswer(answer)
                })
            } else if (this.currentlevel.totalnumber == 80)
            {
                let answ = this.correctAnswer
                answ = 'animation-timing-function: ease-in-out;\nanimation-name: fly;ORanimation-name: fly;\nanimation-timing-function: ease-in-out;'
                answ = answ.split("OR")
                answ.forEach(answer => {
                    this.checkAnswer(answer)
                })
            } else if (this.currentlevel.totalnumber == 81)
            {
                let answ = this.correctAnswer
                answ = 'animation-name: isparenie;\nanimation-delay: 4s;ORanimation-delay: 4s;\nanimation-name: isparenie;'
                answ = answ.split("OR")
                answ.forEach(answer => {
                    this.checkAnswer(answer)
                })
            } else if (this.currentlevel.totalnumber == 82)
            {
                let answ = this.correctAnswer
                answ = 'animation-iteration-count: 1.5;\nanimation-name: fly;ORanimation-name: fly;\nanimation-iteration-count: 1.5;'
                answ = answ.split("OR")
                answ.forEach(answer => {
                    this.checkAnswer(answer)
                })
            } else if (this.currentlevel.totalnumber == 83)
            {
                let answ = this.correctAnswer
                answ = 'animation-iteration-count: infinite;\nanimation-name: fly;ORanimation-name: fly;\nanimation-iteration-count: infinite;'
                answ = answ.split("OR")
                answ.forEach(answer => {
                    this.checkAnswer(answer)
                })
            } else if (this.currentlevel.totalnumber == 84)
            {
                let answ = this.correctAnswer
                answ = 'animation-name: fly;\nanimation-direction: reverse;ORanimation-direction: reverse;\nanimation-name: fly;'
                answ = answ.split("OR")
                answ.forEach(answer => {
                    this.checkAnswer(answer)
                })
            } else if (this.currentlevel.totalnumber == 85)
            {
                let answ = this.correctAnswer
                answ = 'animation-name: fly;\nanimation-direction: alternate;ORanimation-direction: alternate;\nanimation-name: fly;'
                answ = answ.split("OR")
                answ.forEach(answer => {
                    this.checkAnswer(answer)
                })
            } else if (this.currentlevel.totalnumber == 86)
            {
                let answ = this.correctAnswer
                answ = 'animation-name: fly;\nanimation-direction: alternate-reverse;ORanimation-direction: alternate-reverse;\nanimation-name: fly;'
                answ = answ.split("OR")
                answ.forEach(answer => {
                    this.checkAnswer(answer)
                })
            } else if (this.currentlevel.totalnumber == 87)
            {
                let answ = this.correctAnswer
                answ = 'animation-name: fly;\nanimation-iteration-count: 1;\nanimation-fill-mode: forwards;ORanimation-name: fly;\nanimation-fill-mode: forwards;\nanimation-iteration-count: 1;ORanimation-fill-mode: forwards;\nanimation-name: fly;\nanimation-iteration-count: 1;ORanimation-fill-mode: forwards;\nanimation-iteration-count: 1;\nanimation-name: fly;ORanimation-iteration-count: 1;\nanimation-fill-mode: forwards;\nanimation-name: fly;ORanimation-iteration-count: 1;\nanimation-name: fly;\nanimation-fill-mode: forwards;ORanimation-name: isparenie;\nanimation-iteration-count: 1;\nanimation-fill-mode: forwards;ORanimation-name: isparenie;\nanimation-fill-mode: forwards;\nanimation-iteration-count: 1;ORanimation-fill-mode: forwards;\nanimation-name: isparenie;\nanimation-iteration-count: 1;ORanimation-fill-mode: forwards;\nanimation-iteration-count: 1;\nanimation-name: isparenie;ORanimation-iteration-count: 1;\nanimation-fill-mode: forwards;\nanimation-name: isparenie;ORanimation-iteration-count: 1;\nanimation-name: isparenie;\nanimation-fill-mode: forwards;'
                answ = answ.split("OR")
                answ.forEach(answer => {
                    this.checkAnswer(answer)
                })
            } else if (this.currentlevel.totalnumber == 88)
            {
                let answ = this.correctAnswer
                answ = 'animation: round 10s linear 1s infinite normal backwards;'
                this.checkAnswer(answ)
            } 
            this.coding.id = Date.now()
            this.$emit('create', this.coding)
            this.$emit('unclear')
        },
        goNext() {
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
                this.coding.text = ''
                document.getElementById('nextlvl').style="visibility: hidden;"
                document.getElementById('showAnswer').style="visibility: hidden;"
                this.$emit('changelevel', this.newlevel)
                this.$emit('changevisual', this.newvisual)
                this.$emit('changetheory', this.newtheory)
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
                    this.coding.text = ''
                    document.getElementById('nextlvl').style="visibility: hidden;"
                    document.getElementById('showAnswer').style="visibility: hidden;"
                    this.$emit('changevisual', this.newvisual)
                    this.$emit('changelevel', this.newlevel)
                    this.$emit('changetheory', this.newtheory)
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
                        this.coding.text = ''
                        document.getElementById('nextlvl').style="visibility: hidden;"
                        document.getElementById('showAnswer').style="visibility: hidden;"
                        this.$emit('changevisual', this.newvisual)
                        this.$emit('changelevel', this.newlevel)
                        this.$emit('changetheory', this.newtheory)
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
            } else if ((levelnumber >=8 && levelnumber <=26) || (levelnumber == 36)) {
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
            } else if (levelnumber >= 57 && levelnumber <= 66) {
                levelvisualname = 'LevelsTransform'
            } else if (levelnumber >= 67 && levelnumber <= 77) {
                levelvisualname = 'LevelsTransition'
            } else if (levelnumber >= 78 && levelnumber <= 88) {
                levelvisualname = 'LevelsAnimation'
            }
            return levelvisualname
        },
        checkAnswer(corrAnsw){
            if (this.needHelp == true) {
                this.coding.text = corrAnsw
                this.needHelp = false
            }
            let uAnsw = this.coding.text
            if (corrAnsw == uAnsw) 
            {
                if (this.currentlevel.totalnumber == 45)
                {
                    let imgs = document.getElementsByClassName('pictureimg')
                    for (let i = 0; i < imgs.length; i++)
                    {
                        imgs[i].style="height: 100%;"
                    }
                } 
                if (this.currentlevel.totalnumber != 45)
                {
                    let imgs = document.getElementsByClassName('pictureimg')
                    for (let i = 0; i < imgs.length; i++)
                    {
                        imgs[i].style="height: auto;"
                    }
                }
                document.getElementById('nextlvl').style="visibility: visible;"
                document.getElementById('showAnswer').style="visibility: hidden;" 
            }
            else {document.getElementById('showAnswer').style="visibility: visible;"}
        },
        showCorrectAnswer(){
            this.needHelp = true
            this.checkCss()
            document.getElementById('showAnswer').style="visibility: hidden;"
            document.getElementById('nextlvl').style="visibility: visible;"
        },
        clearTextbox() {
            if (this.clearArea == true)
            {
                this.coding.text = ''
            }
        }
    },
    watch: {
        clearArea: function(){
            this.clearTextbox()
        }
    }
    
}
</script>

<style scoped>
.coding{
    display: flex;
    justify-self: flex-end;
    width: 100%;
    /* height: 50%; */
    height: fit-content;
    flex-direction: column;
    background-color: rgb(255, 180, 0);
    align-items: flex-end;
    border: none;
    border-radius: 8px;

}
.code-place{
    width: calc(100% - 40px);
    margin: 20px;
    /* height: calc(100% - 44px - 20px); */
    height: fit-content;
    background-color: rgb(202, 202, 202);
    padding: 8px 12px;
    border: none;
    border-radius: 8px;
    display: flex;
    flex-direction: row;
}
.nextlvl, .showAnswer{
    visibility: hidden;
    color: rgb(255, 180, 0);
    background-color: white;
    border: 2px solid white;
    width: fit-content;
    height: fit-content;
    font-size: 24px;
    padding: 8px 12px;
    border-radius: 8px;
    margin: 0px 20px 20px 20px;
    transition: 0.3s;
}
.buttons{
    display: flex;
    width: 100%;
    justify-content: space-between;
}
.check{
    background-color: rgb(255, 180, 0);
    color: white;
    border: 2px solid white;
    width: fit-content;
    height: fit-content;
    font-size: 24px;
    padding: 8px 12px;
    border-radius: 8px;
    margin: 0px 20px 20px 20px;
    transition: 0.3s;
}
.check:hover, .nextlvl:active, .showAnswer:active{
    background-color: white;
    color: rgb(255, 200, 0);
}
.check:active, .nextlvl:hover, .showAnswer:hover{
    background-color: rgb(255, 180, 0);
    color: chocolate;
}
.stringnumbers{
    display: flex;
    flex-direction: column;
    font-size: 24px;
    color: darkgray;
    font-weight: bold;
    text-align: right;
    margin-right: 8px;
    border-right: 2px solid darkgray;
    height: fit-content;
}
.nums{
    width: 28px;
    padding-right: 4px;
}
#typehere{
    width: calc(100% - 36px);
    height: 100%;
    border-radius: 12px;
    padding-left: 12px;
    font-size: 24px;
    resize: none;
    outline: none;
    overflow: hidden;
}
</style>
