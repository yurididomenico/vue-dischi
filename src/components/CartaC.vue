<template>        
    <a href="#" class="carta">
        <img :src="dettagliCarta.poster" class="mb-3">
        <div>
            <h5>{{dettagliCarta.title}}</h5>
            <p>{{dettagliCarta.author}}</p>
            <p>{{dettagliCarta.year}}</p>
        </div>
    </a>        
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
    color: inherit;
    text-align: center;
    text-decoration: none;
    width: calc(100% / 5 - 40px);   
         
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
    &:hover
    {
        scale: 1.2;
        transition-duration: 300ms;
    }
    
  }
  </style>