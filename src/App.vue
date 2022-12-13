<template>
  <div id="app">
    <!-- <register-ecommerce ></register-ecommerce>
    <div v-for="(dato, index) in datos" :key="index"> 
      <login-ecommerce></login-ecommerce>
    </div> -->
    <!-- <list-ecommerce :products="datos"></list-ecommerce> -->
    <!-- <detalle-item :product="datos[0]"></detalle-item> -->
  <carrito-ecommerce :product="datos[0]"></carrito-ecommerce>
  </div>
</template> 
<script>
// import RegisterEcommerce from './components/Ecommerce/RegisterEcommerce.vue'
// import LoginEcommerce from './components/Ecommerce/LoginEcommerce.vue';
// import ListEcommerce from './components/Ecommerce/ListEcommerce.vue';
// import DetalleItem from './components/Ecommerce/DetalleItem.vue';
import imagen from './assets/4d95ee421422145ef856c040751d4386.jpg'
import CarritoEcommerce from './components/Ecommerce/CarritoEcommerce.vue';

export default {
  name: 'App',
  data() {
    return {
      datos: [{ price: 2000, src: imagen, title: 'Papas Fritas', text: "Disfruta de las mejores papas fritas del mercado", description: "Lorem ipsum, dolor sit amet consectetur adipisicing elit. Animi doloribus corrupti quis temporibus error perspiciatis rem. Eos modi qui libero, pariatur quam doloremque laboriosam reprehenderit id saepe. Eum, tenetur accusantium" },
        { src: imagen, title: 'Salsa de Tomate', text: "Este es un texto" },
        { src: imagen, title: 'Salsa de Tomate', text: "Este es un texto" }],
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
    // RegisterEcommerce,
    // LoginEcommerce,
    // ListEcommerce,
    // DetalleItem,
    CarritoEcommerce
    
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
  display: flex;
  align-items: center;
}
</style>