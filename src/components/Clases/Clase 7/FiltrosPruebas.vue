<template>
    <div>
        <h1>Lista de precios redondeados</h1>
        <p v-for="(precio, index) of listaPrecios" :key="index">${{precio | redondear}}</p>
    </div>
</template>
  
  <script>
  export default {
    name: 'FiltrosPrueba',
    data() {
        return {
            listaPrecios:[1299.9999, 10870.8989, 34000, 9899-9090]
        }
    },
    filters: {
        redondear:(precio) => {
            return precio.toFixed(2)
        }
    }
  }
  </script>
  
  <!-- Add "scoped" attribute to limit CSS to this component only -->
  <style scoped>

  </style>
  