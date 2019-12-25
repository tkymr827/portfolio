<template>
    <div class="content">
        <div class="left"><img src="../assets/relaxsounds.gif"></div>
        <div class="right">
        <h1>Relax Sounds</h1>
        <p>Vue.jsを使って初めて作ってみたやつ<br>
            ディレクティブの使い方やJavaScriptの初歩的な使い方を学べたと思う<br>
            <span>制作期間：３日ぐらい?</span></p>
            <a href="https://tkymr827.github.io/relax-sounds/" target="_blank">サイトはこちらから</a>
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
