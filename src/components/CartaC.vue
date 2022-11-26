<template>
    
        <!-- <div class="card border-0 rounded-0 p-4 m-0">
            <img src="https://i.stack.imgur.com/xJida.png" class="card-img-top rounded-0 " alt="...">
            <div class="card-body">
                <h5 class="card-title text-white fs-2 mb-3">TITOLO</h5>
                <p class="card-text text-secondary fs-4 mb-0">Artista</p>
                <p class="text-secondary p-0">Anno</p>
            </div>
        </div> -->

        <div class="carta">
            <img :src="dettagliCarta.poster" class="mb-3">
            <div>
                <h5>{{dettagliCarta.title}}</h5>
                <p>{{dettagliCarta.author}}</p>
                <p>{{dettagliCarta.year}}</p>
            </div>
        </div>
        
</template>
  
  <script>
  
  
  export default {
    name: 'CartaC',
    props: {
        dettagliCarta: Object
    }
  }
  </script>
  
  <!-- Add "scoped" attribute to limit CSS to this component only -->
  <style scoped lang="scss">
  .carta
  {
    background-color: #2e3a46;
    text-align: center;
    // width: 250px;
    width: calc(100% / 5 - 40px);
    // margin-bottom: 40px;
    
    
    img
    {
        width: 100%;
        aspect-ratio: 1/1;
        display: hidden;
        
    }
    
    p
    {
        color: grey;
    }
  }
  </style>
  