<template>
  <div id="app">

  <!--
  <div class="placeholder" > </div>
  <div class="placeholder">BVG/VBB</div>
  <div class="placeholder">Einkaufsliste/Flatastic</div>
  <div class="placeholder">Putzplan/Flatastic</div>
  <div class="placeholder">Calendar</div>
  -->

    <Clock class='widget clock' msg="This is Clock placeholder"/>
    <Flatastic class='widget' msg="This is Flatastic placeholder"/>
    <Calendar class='widget' msg="This is Calendar placeholder"/>
    <VBB class='widget' msg="This is VBB placeholder"/>
    <Clock class='widget' msg="This is Clock placeholder"/>
    <VBB class='widget' msg="This is Wetter placeholder"/>

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

body{
  background-color: #000;
  margin: 0;
}
#app {
  background-color: #000;

  display: grid;
  grid-template-columns:  50% 50%;
  grid-template-rows: 33.33% 33.33% 33.33%;
  /*   */
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #fff;
  font-size: 20px;
height: 100vh;
}

.widget-container{

  padding: 10px;
  border: 1px solid white;
;

}
.clock{
  font-size: 60px;

}

</style>
