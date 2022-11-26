<template>
  <div id="BodyC" class="p-5">
    <div class="container py-5 d-flex flex-wrap justify-content-around ">
      <CartaC v-for="(elem, index) in arrayTest"
      :key="index"
      :dettagliCarta="elem"/>
    </div>
  </div>
</template>

<script>
import axios from 'axios'
import CartaC from '../components/CartaC.vue'

export default {
  name: 'BodyC',
  components: {
    CartaC
  },
  data() {
      return {
        arrayTest: ""
      }
  },
  mounted()
  {
    
    // console.clear();
    axios.get('https://flynn.boolean.careers/exercises/api/array/music').then((response) =>
    {
      this.arrayTest = response.data.response;
      response.data.response[0].poster = "https://s7.orientaltrading.com/is/image/OrientalTrading/16_878d?$PDP_VIEWER_IMAGE$";
      response.data.response[0].author = "Four Duck Developers";
      response.data.response[0].title = "What a DUCK?!";
      response.data.response[0].year = "2022";

      
      console.log(response.data.response);
    })
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
#BodyC
{
  background-color: #1e2d3b;
}

.container
{
  gap: 50px;
  
}
</style>
