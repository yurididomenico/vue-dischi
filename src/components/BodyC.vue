<template>
  <div id="BodyC" class="p-5">
    <div  class="container py-5">
      <div class="d-flex flex-wrap ">
        <CartaC v-for="(elem, index) in 10" :key="index"/>
      </div>
    </div>
  </div>
</template>

<script>
import CartaC from '../components/CartaC.vue'

export default {
  name: 'BodyC',
  components: {
    CartaC
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
#BodyC
{
  background-color: #1e2d3b;
}
</style>
