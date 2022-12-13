<template>
    <div class="container d-flex justify-content-center align-items-center">    
  <div class="row">
    <div class="col-sm-7">
      <img v-bind:src="product.src" alt="">
    </div>
    <div class="col-sm-4">
      <h3 class="mb-5"> {{product.title}}</h3>
      <p class="mt-5"> {{product.description}}</p>
      <div class="row align-items-center"> 
        <div class="col-sm-6 mt-3">
          <h5>Precio: ${{product.price}}</h5>
        </div>
        <div class="col-sm-6">
          <button type="button" class="btn btn-primary">Agregar al carro</button>
        </div>
      </div>
    </div>
  </div>
  </div>
</template>
  
  <script>
export default {
  name: 'DetalleItem',
  props: {
    product: Object
  },
  data() {
    return {
      title: '',
      email_address: '',
    };
  },
}
  </script>
  
  <!-- Add "scoped" attribute to limit CSS to this component only -->
  <style scoped>

img 
  { width: 500px;
    height: 500px;}

  </style>