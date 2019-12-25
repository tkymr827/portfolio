<template>
    <div class="content">
        <div class="left"><img src="../assets/numgame.gif"></div>
        <div class="right">
        <h1>Number Game</h1>
        <p>JavaScriptの勉強ついでに作ってみたゲーム<br>
            数字をランダムに配置してクリックした順番を判定するのが大変だった<br>
            本当はランキング形式にしたかったけどソートがうまくできなくてスコア表になった(でも動きおかしい)<br>
            <span>制作期間：5日ぐらい</span></p>
            <a href="https://tkymr827.github.io/num-game/" target="_blank">サイトはこちらから</a>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.content{
    display:flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    .left{
        margin:-5rem auto 0 auto;
        img{
            height:40rem;
        }
    }
    .right{
        text-align: center;
        font-size:1.2rem;
        p{
            font-size:1.5rem;
            span{

                color:gray;
            }
        }
    }
}
</style>
