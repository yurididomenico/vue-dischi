<template>
  <div id="BodyC" class="p-5">
    <div class="container d-flex align-items-center">
      <h3>Filtra:</h3>
      <select class="form-select w-25 " aria-label="Default select example" v-model="scelta" @click="test()">
        <option value="">Tutti</option>
        <option v-for="(elem, index) in vettoreGeneri" :key="index">{{elem}}</option>     
      </select>
    </div>
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
        arrayTest: [],
        vettoreGeneri: [],
        vettoreFiltrato: [],
        scelta: ""
      }
  },
  mounted()
  {    
    // console.clear();
    axios.get('https://flynn.boolean.careers/exercises/api/array/music').then((response) =>
    {
    
      response.data.response.forEach(element => {
        if(!this.vettoreGeneri.includes(element.genre))
        {
          this.vettoreGeneri.push(element.genre)
        }
      });

      this.arrayTest = response.data.response;
      this.arrayTest[0].poster = "https://s7.orientaltrading.com/is/image/OrientalTrading/16_878d?$PDP_VIEWER_IMAGE$";
      this.arrayTest[0].author = "Four Ducks Developers";
      this.arrayTest[0].title = "What a DUCK?!";
      this.arrayTest[0].year = "2022";
    
    })
  },
  beforeUpdate()
  {
    if(this.scelta == '')
      {
        return this.arrayTest
      }
      else
      {
        this.vettoreFiltrato = 
        this.arrayTest.filter((elem) =>
        {
          return elem.genre == this.scelta
        });
        return this.vettoreFiltrato
      }
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