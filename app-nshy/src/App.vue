<template>
  <header>
    <the-header :cartList="cartList" />
  </header>
  <main class="container">
    <product-list @hanlde-buy="hanldeBuy" />
  </main>
</template>

<script>
import TheHeader from './components/TheHeader.vue';
import ProductList from './components/ProductList.vue';

export default {
  name: 'App',
  components: {
    TheHeader,
    ProductList,
  },
  data() {
    return {
      cartList: [],
    }
  },
  methods: {
    hanldeBuy(productItem) {
      console.log(productItem);
      // this.cartList.push(productItem);
      this.cartList = [...this.cartList, productItem];
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
