<template>
    <div class="container-fluid">
    <h1>{{titulo}}</h1>
    <div class="row p-4">
        <hijo-prueba :titulo="tit_hijo" @enviar="frases.push($event)"> </hijo-prueba>
        <card-frase v-for="(frase, index) of frases" :key="index" :frase="frase" :indice="index"></card-frase>
    </div>
    </div>
  </template>
  
  <script>
    import CardFrase from './CardFrase.vue'
    import HijoPrueba from './HijoPrueba.vue';

  export default {
    name: 'PadrePrueba',

    data() {
        return {
            titulo: "g",
            frases: ["abc"],
            tit_hijos: "Ingrese"
        }
    },
    components: {
        CardFrase,
        HijoPrueba
    }
  }
  </script>
  
  <!-- Add "scoped" attribute to limit CSS to this component only -->
  <style scoped>

  </style>
  