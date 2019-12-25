<template>
    <div id="overlay">
        <div class="content">
            <relaxsounds v-if="val === 1"/>
            <weathernow v-else-if="val === 2"/>
            <numbergame v-else-if="val === 3"/>
            <div class="close" @click="close">Close</div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
#overlay{
        position: fixed;
        top:0;
        left:0;
        height:100%;
        width:100%;
        background:rgba(0,0,0,.6);
        z-index: 1;
        display: flex;
        justify-content: center;
        align-items: center;
    .content{
        z-index: 2;
        height:60rem;
        width:90rem;
        background:beige;
        position: relative;
        border-radius:3rem;
        .close{
            @media screen  and(max-width: 1100px){
                right:30%;
            }
            position: absolute;
            bottom:2rem;
            right:2rem;
            font-size:2rem;
            background:#2e2e2e;
            color:rgb(250, 175, 35);
            padding:1rem 3rem;
            border-radius: 20%;
            cursor: pointer;
            z-index: 3;
        }
    }
}
</style>

<script>
import relaxsounds from './relaxsounds.vue'
import weathernow from './weathernow.vue'
import numbergame from './numbergame.vue'
export default {
  components: {
    relaxsounds,
    weathernow,
    numbergame
  },
  props: ['val'],
  data () {
    return {
      modal: true
    }
  },
  methods: {
    close: function () {
      this.$emit('close')
    }
  }
}
</script>
