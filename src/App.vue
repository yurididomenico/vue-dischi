<template>
  <div id="app">
    <HeaderC/>
    <BodyC/>
  </div>
</template>

<script>
import HeaderC from './components/HeaderC.vue'
import BodyC from './components/BodyC.vue'



import axios from 'axios';

export default {
  name: 'App',
  components: {
    HeaderC,
    BodyC
  },
  data() {
    return {

    }
  },
  mounted()
  {
    axios.get('https://flynn.boolean.careers/exercises/api/array/music').then((res) =>
    {
    console.log(res);
    })
  }
}
</script>

<style lang="scss">

</style>
