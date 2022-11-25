<template>
  <div id="app" class="bg-primary">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'


import 'bootstrap/dist/css/bootstrap.min.css'
import 'bootstrap/dist/js/bootstrap.min.js'
import axios from 'axios';

export default {
  name: 'App',
  components: {
    HelloWorld
  },
  data()
  {
    return
    {

    }
  },
  mounted()
  {
    axios.get('https://flynn.boolean.careers/exercises/api/array/music')
         .then((res) =>
         {
          console.log(res);
         })
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
