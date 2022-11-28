<!--
  Descrizione:
  Aggiungere una select per filtrare i dischi
  in base al genere:
    -quando l'utente seleziona un 
    genere dalla lista, vengono visualizzati
    solamente i dischi con il genere
    corrispondente.
-->

<template>
  <div id="app" class="d-flex flex-column">
    <HeaderC/>
    <BodyC class="flex-grow-1"/>
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
    height: 100vh;
  }
</style>
