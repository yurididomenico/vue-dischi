<template>
    <div>
        <div class="card border-0 rounded-0 p-4">
            <img src="https://i.stack.imgur.com/xJida.png" class="card-img-top rounded-0 " alt="...">
            <div class="card-body">
                <h5 class="card-title text-white fs-2 mb-3">TITOLO</h5>
                <p class="card-text text-secondary fs-4 mb-0">Artista</p>
                <p class="text-secondary p-0">Anno</p>
            </div>
        </div>

        
    </div>
  </template>
  
  <script>
  
  
  export default {
    name: 'CartaC',
  }
  </script>
  
  <!-- Add "scoped" attribute to limit CSS to this component only -->
  <style scoped lang="scss">
  .card
  {
    background-color: #2e3a46;
    text-align: center;
    width: calc(100% / 3 );
    
    
    img
    {
        aspect-ratio: 1/1;
    }
  }
  </style>
  