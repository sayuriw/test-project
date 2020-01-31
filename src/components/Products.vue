<template>
  <div>
    <h1>My Shop</h1>
    <navbar
      :cart="cart"
      :cartQty="cartQty"
      :cartTotal="cartTotal"
    ></navbar
      >
    <price-slider
      :sliderStatus="sliderStatus"
      :maximum.sync="maximum"
    ></price-slider>
    <product-list
      :products="products"
      :maximum="maximum"
    ></product-list>
  </div>
</template>

<script>
import Navbar from './Navbar.vue'
import PriceSlider from './PriceSlider.vue'
import ProductList from './ProductList.vue'

export default {
  name: 'products',
  components: {
    Navbar, 
    PriceSlider, 
    ProductList
  },
  props: ['cart', 'cartQty', 'cartTotal', 'sliderStatus','sliderState', 'maximum', 'products']


}

</script>