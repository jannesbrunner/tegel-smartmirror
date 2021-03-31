<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <VBB msg="This is VBB placeholder"/>
    <Clock msg="This is Clock placeholder"/>
    <Flatastic msg="This is Flatastic placeholder"/>
    <Calendar msg="This is Calendar placeholder"/>
  </div>
</template>

<script>
import VBB from './components/VBB.vue'
import Clock from './components/Clock.vue'
import Flatastic from './components/Flatastic.vue'
import Calendar from './components/Calendar.vue'

export default {
  name: 'App',
  components: {
    VBB,
    Clock,
    Flatastic,
    Calendar
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
