<template>
  <div id="app" >
  </div>
</template>

<script>
// import ConMixin from './components/Clases/Clase 7/ConMixin.vue'
// import HelloWorld from './components/Clases/Clase 7/HelloWorld.vue'
// import SlotPrueba from './components/Clases/Clase 7/SlotPrueba.vue'
// import PadrePrueba from './components/Clases/Clase 7/PadrePrueba.vue'
// import FiltrosPruebas from './components/Clases/Clase 7/FiltrosPruebas.vue'
// import FormularioWeb from './components/Clases/Clase 8/FormularioWeb.vue'
// import TableEcommerce from './components/Clases/Clase 7/TableEcommerce.vue'
import RegisterEcommerce from './components/Ecommerce/RegisterEcommerce.vue'

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
      featureItems: [{ label: "Envio gratutito", href: "img/features/f1.png"},
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