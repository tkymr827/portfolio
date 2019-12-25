<template>
    <div class="content">
        <div class="left"><img src="../assets/weathernow.png"></div>
        <div class="right">
        <h1>Weather Now</h1>
        <p>SPAとAPIを使って作ってみたサイト<br>
            本当はもっと多くの地域を取得したかったがAPI制限の問題で断念<br>
            拘ったところは天気によって背景画像が変わるところ
            <span>制作期間：5日ぐらい</span></p>
            <a href="https://tkymr827.github.io/weathernow/#/" target="_blank">サイトはこちらから</a>
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
