<template>
  <h2>Volume Tracker (0-20)</h2>
  <h2>Current Volume - {{ volume }}</h2>
  <div d-flex >
    <button @click="volume += 2">Increase</button>
    <button @click="volume -= 2">Decrease</button>
  </div>
</template>

<script>

export default {
  name: 'App',
  data(){
    return {
      volume: 0
    }
  },
  methods: {},
  computed: {},
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
