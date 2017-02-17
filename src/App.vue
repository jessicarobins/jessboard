<template>
  <div id="app">
    <jessboard></jessboard>
  </div>
</template>

<script>
import Hello from './components/Hello'
import Jessboard from './components/Jessboard'

export default {
  name: 'app',
  components: {
    Hello,
    Jessboard
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
