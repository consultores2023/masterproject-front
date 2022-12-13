<template>
    <div class="container d-flex justify-content-between">
      <div v-for="(product, index) in products" :key="index">
        <div class="card" style="width: 18rem;">
        <img class="card-img-top" v-bind:src="product.src" alt="Card image cap">
        <div class="card-body">
          <h5 class="card-title">{{product.title}}</h5>
          <p class="card-text">{{product.text}}</p>
          <a href="#" class="btn btn-primary">Go somewhere</a>
        </div>
        </div>
      </div>
    </div>
</template>
  
  <script>
export default {
  name: 'ListEcommerce',
  props: {
    products: Array
  },
  data() {
    return {
      password: '',
      email_address: ''
    };
  },
}
  </script>
  <!-- Add "scoped" attribute to limit CSS to this component only -->
  <style scoped>

  </style>