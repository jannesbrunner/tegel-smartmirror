<template>
  <div class="widget-container">
    <transition name="list-complete">
    <h1>{{ hour }}:{{ minute }}:{{ second }}</h1>
    </transition>
    <!--<ul>
      <li v-for="x in lol">{{x}}</li>
      <p v-if="kkk">Jo</p>
    </ul>
    -->

  </div>
</template>

<script>

export default {
  name: 'HelloClock',
  props: {
    msg: String
  },
  data () {
    return {
      clock: null,
      hour: null,
      minute: null,
      second: null,
      lel: 5,
      lol: [1, 2, 3, 4, 5],
      clockIntervall: null

    }
  },
  mounted () {
    this.clockIntervall = setInterval(this.getTime, 1000)
  },
  beforeUnmount () {
    clearInterval(this.clockIntervall)
  },
  methods: {
    countUp (x) {
      return x + 1 + this.lel
    },

    getTime () {
      var clock = new Date()
      var hours = clock.getHours()
      hours = hours < 10 ? '0' + hours : hours
      var minutes = clock.getMinutes()
      minutes = minutes < 10 ? '0' + minutes : minutes
      var seconds = clock.getSeconds()
      seconds = seconds < 10 ? '0' + seconds : seconds
      this.hour = hours
      this.minute = minutes
      this.second = seconds
    },

    updateClock () {

    }
  },
  computed: {

  }

}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}

.list-complete-item {
  transition: all 0.8s ease;
  display: inline-block;
  margin-right: 10px;
}

.list-complete-enter-from{
  opacity:0;
  transform:translateY(-30px);
}
.list-complete-leave-to {
  opacity: 0;
  transform: translateY(30px);
}

.list-complete-leave-active {
  position: absolute;
}

</style>
