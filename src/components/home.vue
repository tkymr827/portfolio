<template>
    <main>
        <overlay :val="overlayshow" @close="modalon" v-if="modal"/>

        <h1>作ったものたち</h1>
        <nav>
            <!-- router-link置く -->
        </nav>
        <div class="conteiner">
            <div class="box">
                <div class="front"><img src="../assets/relaxsounds.png"></div>
                <div class="back">
                    <span></span>
                    <span></span>
                    <span></span>
                    <span></span>
                    <h3>Relax Sounds</h3>
                    <p>リラックスできるBGMが再生されるサイトです。</p>
                    <div class="more" @click="modalon(1)">MORE</div>
                </div>
            </div>
            <div class="box">
                <div class="front"><img src="../assets/weathernow.png"></div>
                <div class="back">
                    <span></span>
                    <span></span>
                    <span></span>
                    <span></span>
                    <h3>Weather Now</h3>
                    <p>現在の東京・北海道・ニューヨーク・リオデジャネイロの天気が見れます。</p>
                    <div class="more" @click="modalon(2)">MORE</div>
                </div>
            </div>
            <div class="box">
                <div class="front"><img src="../assets/numgame.png"></div>
                <div class="back">
                <span></span>
                <span></span>
                <span></span>
                <span></span>
                    <h3>Number Game</h3>
                    <p>数字を順番に押してくゲームです。</p>
                    <div class="more" @click="modalon(3)">MORE</div>
                </div>
            </div>
             <div class="box">
                <div class="front"></div>
                <div class="back">
                    <span></span>
                    <span></span>
                    <span></span>
                    <span></span>
                    <h3>工事中</h3>
                    <p>工事中</p>
                    <p>工事中</p>
                    <p>工事中</p>
                    <div class="more" @click="modalon(4)">MORE</div>
                </div>
            </div>
        </div>
    </main>
</template>

<style lang="scss" scoped>

main{
    @media screen and (max-width:1100px){
        height:0;
    }
    height:100vh;
    background: #f9fbb1 ;
    color:#0d084e;
    position: relative;
    margin:0 15rem;
    h1{
        height:10rem;
        line-height:10rem;
    }
    .conteiner{
        @media screen and(max-width:1100px){
            height:0;
        }
        position: absolute;
        bottom:0;
        // background:red;

        height:70rem;
        width:100%;

        display:flex;
        justify-content: space-evenly;
        align-items: center;
        flex-wrap: wrap;
        .box{
            @media screen and (max-width:1100px){
                margin:3rem 0;
            }
            height:30rem;
            width:40rem;
            &:hover .front{
                transform: rotateX(180deg);
            }
            &:hover .back{
                transform: rotateX(0);
            }
            &:hover span:nth-child(1){
                    animation: animate1 2s ease-in-out infinite;
            }
            &:hover span:nth-child(2){
                    animation: animate2 2s ease-in-out infinite;
                    animation-delay: 1s;
            }
            &:hover span:nth-child(3){
                    animation: animate3 2s ease-in-out infinite;
            }
            &:hover span:nth-child(4){
                    animation: animate4 2s ease-in-out infinite;
                    animation-delay: 1s;
            }
            .front,.back{
                background:black;
                height:30rem;
                width: 40rem;
                position: absolute;
                transition:1s;
                backface-visibility: hidden;
            }
            img{
                height:30rem;
                width:40rem;
            }
            .back{
                background:#72C3CD;
                transform:rotateX(180deg);
                position: relative;
                overflow: hidden;

                display: flex;
                justify-content: center;
                align-items: center;
                flex-direction: column;

                padding:4rem;
                h3{
                    font-size:2.3rem;
                }
                p{
                    font-size:1.5rem;
                    padding-top:1.5rem;
                }
                span {
                position: absolute;
                    &:nth-child(1) {
                        top: 0;
                        left:0;
                        height: 0.4rem;
                        width: 100%;
                        background: linear-gradient(to right,#72C3CD,#EB0E82);
                        transform: translateX(100%);
                    }
                    &:nth-child(2) {
                        right: 0;
                        top:0;
                        height: 100%;
                        width: 0.4rem;
                        background: linear-gradient(to bottom,#72C3CD,#EB0E82);
                        // animation: animate2 2s ease-in-out infinite;
                        // animation-delay: 1.1s;
                        transform: translateY(-100%);
                    }
                    &:nth-child(3) {
                        left:0;
                        bottom: 0;
                        height: 0.4rem;
                        width: 100%;
                        background: linear-gradient(to left,#72C3CD,#EB0E82);
                        // animation: animate3 2s ease-in-out infinite;
                        transform: translateX(-100%);
                    }
                    &:nth-child(4) {
                        top:0;
                        left: 0;
                        height: 100%;
                        width: 0.4rem;
                        background: linear-gradient(to top,#72C3CD,#EB0E82);
                        // animation: animate4 2s ease-in-out infinite;
                        transform: translateY(-100%);
                        // animation-delay: 1s;
                    }
        }

                .more{
                    position: absolute;
                    bottom:2rem;
                    right:2rem;
                    font-size:2rem;
                    background:#2e2e2e;
                    color:rgb(250, 175, 35);
                    padding:1rem 3rem;
                    border-radius: 20%;
                    cursor: pointer;
                }
            }
        }
    }
}
@keyframes animate1 {
    to {
        transform: translateX(100%);
    }
    from {
        transform: translateX(-100%);
    }
}
@keyframes animate2 {
    to {
        transform: translateY(100%);
    }
    from {
        transform: translateY(-100%);
    }
}
@keyframes animate3 {
    to {
        transform: translateX(-100%);
    }
    from {
        transform: translateX(100%);
    }
}
@keyframes animate4 {
    to {
        transform: translateY(-100%);
    }
    from {
        transform: translateY(100%);
    }
}

</style>

<script>
import overlay from './modal.vue'
export default {
  components: {
    overlay
  },
  data () {
    return {
      modal: false,
      overlayshow: 0
    }
  },
  methods: {
    modalon: function (index) {
      this.modal = !this.modal
      this.overlayshow = index
    //   alert(this.overlayshow)
    }
  }

}
</script>
