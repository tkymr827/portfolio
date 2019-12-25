<template>
<transition name="pageon">

    <main v-if="pageon">
        <div class="content">
            <h1>Portfolio Site</h1>
            <div class="join" v-on:click="change">ENTER</div>
        </div>
    </main>
</transition>
</template>

<style lang="scss" scoped>
main{
    z-index: 100;
    position: fixed;
    display:flex;
    justify-content: center;
    align-items: center;
    height:80vh;
    width:100%;
    &::before{
        content:"";
        position: absolute;
        width:100%;
        height:100%;
        background:linear-gradient(to top ,#dac8a3,rgb(233, 88, 88) );
        border-radius: 0 0 50% 50% / 0 0 100% 100%;
        transform: scaleX(1.5)
    }
    .content{
        position: relative;
        text-align: center;
        h1{
            color:#243a63;
            font-size:6rem;
        }
        .join{
            color:#243a63;
            font-size:3rem;
            border:#fff solid .2rem;
            display: inline-block;
            padding:1.5rem 5rem;
            margin-top:5rem;
            cursor: pointer;
            transition: .5s;
            &:hover{
                background:#243a63;
                color:#fff;
        }}
    }
}
.pageon-leave-active{
    animation:pageon 1s forwards;
}
@keyframes pageon {
    from{
        transform: translateY(0);
    }
    to{
        transform: translateY(-80vh);
        display: none;
    }
}
</style>

<script>
export default {
  data () {
    return {
      pageon: true
    }
  },
  methods: {
    change: function () {
      this.pageon = false
      this.$emit('change')
    //   alert('ok')
    }
  }

}
</script>
