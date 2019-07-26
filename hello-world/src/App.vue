<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld
      :msg={aTestDataVar}
      :aList={aList}
      v-on:parentAlert="parentAlert"
    />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'app',
  components: {
    HelloWorld
  },
  methods: {
    parentAlert: () => {
      alert('Alert On Parent: You Just Click a button inside child')
    }
  },
  data: function () {
    return {
      aTestDataVar: 7,
      aList: [
        { text: 1 },
        { text: 2 },
        { text: 3 },
      ]
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
