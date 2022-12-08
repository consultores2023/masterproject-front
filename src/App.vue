<template>
  <div id="app">
    <!-- props $refs -->
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <!-- emit -->
    <padre-prueba />
    <!-- slots -->
    <slot-prueba>
      <h3>Osito mediante slot </h3>
      <img src="data:image/jpeg;base64,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" alt="">
      <p slot="precio">${{precio}}</p>
    </slot-prueba>
    <!-- filtros -->
    <filtros-pruebas></filtros-pruebas>
    <!-- filtro-global -->
    <h4>{{ frase | formatFrase }}</h4>
    <!-- mixins -->
    <con-mixin :fecha="new Date()" />
    <formulario-web></formulario-web>

    <table-ecommerce :objetos="featureItems" :style="estilo3" :th_color="estilo4" :background_color="estilo7"></table-ecommerce>
    <table-ecommerce :objetos="productItems" :style="estilo3" :th_color="estilo5" :background_color="estilo8"></table-ecommerce>
    <table-ecommerce :objetos="navbarItems"  :style="estilo3" :th_color="estilo6" :background_color="estilo9" ></table-ecommerce>
  </div>
</template>

<script>
import ConMixin from './components/Clases/Clase 7/ConMixin.vue'
import HelloWorld from './components/Clases/Clase 7/HelloWorld.vue'
import SlotPrueba from './components/Clases/Clase 7/SlotPrueba.vue'
import PadrePrueba from './components/Clases/Clase 7/PadrePrueba.vue'
import FiltrosPruebas from './components/Clases/Clase 7/FiltrosPruebas.vue'
import FormularioWeb from './components/Clases/Clase 8/FormularioWeb.vue'
import TableEcommerce from './components/Clases/Clase 7/TableEcommerce.vue'

export default {
  name: 'App',
  data() {
    return {
      usuario: { nombre: "José Luis Rivas", edad: 34 },
      precio: 2399,
      frase: "Frase para filtro global",
      estilo1: { fontSize: '10px',  'flex-direction': 'row', 'margin': '10px'},
      estilo2: { fontSize: '10px', 'flex-direction': 'row', 'margin': '10px' },
      estilo3: { fontSize: '15px',  'flex-direction': 'row', 'margin': '10px'},
      estilo4: { color: 'red'},
      estilo5: { color: '#6DF743' },
      estilo6: { color: '#00B9AE' },
      estilo7: { 'background-color': '#02C3BD' },
      estilo8: { 'background-color': '#037171' },
      estilo9: { 'background-color': '#03312E' },
      navbarItems: [
            { label: "Shop", href: "shop.html" },
            { label: "About", href: "about.html" },
            { label: "Blog", href: "blog.html" },
            { label: "Contact", href: "contact.html" },
            { label: "Cart", href: "cart.html" }],
      featureItems: [{ label: "Envio gratutito", href: "img/features/f1.png" },
                        { label: "Orden Online", href: "img/features/f2.png" },
                        { label: "Ahorra Dinero", href: "img/features/f3.png" },
                        { label: "Promotions", href: "img/features/f4.png" },
                        { label: "Happy Sell", href: "img/features/f5.png" },
                        { label: "24/7 Support", href: "img/features/f6.png" }],
      productItems: [{ brand: "adidas", name: "Cartoon Astronaut T-shirt", price: "$78", href: "img/products/f1.jpg" },
            { brand: "adidas", name: "Cartoon Astronaut T-shirt", price: "$78", href: "img/products/f2.jpg" },
            { brand: "adidas", name: "Cartoon Astronaut T-shirt", price: "$78", href: "img/products/f3.jpg" },
            { brand: "adidas", name: "Cartoon Astronaut T-shirt", price: "$78", href: "img/products/f4.jpg" },
            { brand: "adidas", name: "Cartoon Astronaut T-shirt", price: "$78", href: "img/products/f5.jpg" },
            { brand: "adidas", name: "Cartoon Astronaut T-shirt", price: "$78", href: "img/products/f6.jpg" },
            { brand: "adidas", name: "Cartoon Astronaut T-shirt", price: "$78", href: "img/products/f7.jpg" },
            { brand: "adidas", name: "Cartoon Astronaut T-shirt", price: "$78", href: "img/products/f8.jpg" }],
        
    }
  },
  components: {
    HelloWorld,
    SlotPrueba,
    PadrePrueba,
    FiltrosPruebas,
    ConMixin,
    FormularioWeb,
    TableEcommerce
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>