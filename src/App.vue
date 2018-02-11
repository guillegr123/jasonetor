<template>
  <div id="app">
    <img src="./assets/logo.png">
    <router-view ref="app" />
  </div>
</template>

<script>
export default {
  name: 'App',
  methods: {
    loadJson (json) {
      alert('JSON loaded')
    }
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
