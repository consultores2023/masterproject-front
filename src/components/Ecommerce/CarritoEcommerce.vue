<template>
    <div class="container d-flex justify-content-center align-items-center">
      <div class="row">
        <div class="col-sm-7">
          <img v-bind:src="product.src" alt="">
        </div>
        <div class="col-sm">
          <div class="row mt-5">
            <div class="col-sm-6">
              <h2>Precio: </h2>
              <h2>Cantidad: </h2>
              <h2>Monto final: </h2>
            </div>
            <div class="col-sm-4">
              <h2>{{product.price}}</h2>
              <input class="mt-2 mb-2" type="number" v-model="cantidad"/>
              <h2>{{mostrarTotal}}</h2>
            </div>
          </div>
        </div>
      </div>
      <div class="row">
        <button type="button" class="btn btn-primary" @click="mostrarAlerta()">Comprar</button>
      </div>
    </div>
</template>

  <script>

export default {
  name: 'CarritoEcommerce',
  props: {
    product: Object,
  },
  data() {
        return {
            cantidad: 1
        };
  },
  methods: {
    mostrarAlerta() {
     alert("Compra realizada") 
    }
  },
  computed: {
    mostrarTotal() {
      return parseInt(this.product.price) * parseInt(this.cantidad);
    },

  }
}
  </script>
  
  <!-- Add "scoped" attribute to limit CSS to this component only -->
  <style scoped>
img 
  { width: 500px;
    height: 500px;}
  </style>