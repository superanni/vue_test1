<template>
  <div id="app">
    <img src="./assets/logo.png">
    <router-view/>
  </div>
</template>

<script>
const axios = require('axios')
export default {
  name: 'App',
  data () {
    return {

    }
  },
  // axios实现跨域
  created () {
    // eslint-disable-next-line no-undef
    axios.post('api/testSpringBoot').then(function (res) {
      console.log(res.data)
    })
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
