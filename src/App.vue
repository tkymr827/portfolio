<template>
  <div id="app">
      <pageon v-on:change="start" />
      <transition>
      <home v-if="fadein"/>
      </transition>
  </div>
</template>
<script>
import pageon from './components/pageon.vue'
import home from './components/home.vue'
export default {
  name: 'app',
  components: {
    pageon,
    home
  },
  data () {
    return {
      fadein: false
    }
  },
  methods: {
    start: function () {
      this.fadein = true
    }
  }
}
</script>

<style lang="scss">
#app {
    background: #f9fbb1 ;
.v-enter{
    opacity: 0;
}
.v-enter-active{
    transition: opacity 2s;
    transition-delay: 1s;
}
}
</style>
