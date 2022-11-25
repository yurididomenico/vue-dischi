<template>
  <div id="app">
    <HeaderC/>
    <BodyC/>
  </div>
</template>

<script>

import HeaderC from './components/HeaderC.vue'
import BodyC from './components/BodyC.vue'

export default {
  name: 'App',
  components: {
    HeaderC,
    BodyC
  }
}
</script>

<style lang="scss">
  #app
  {
    color: white;
  }
</style>
