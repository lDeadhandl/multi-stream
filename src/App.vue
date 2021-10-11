<template>
  <div id="app">
    <MultiStream msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import '../lib/twitch.v1.js'
import MultiStream from './components/MultiStream.vue'

export default {
  name: 'App',
  components: {
    MultiStream
  }
}

</script>

<style>
#app {
  height: inherit;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
