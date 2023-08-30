<template>
    <div class="product-padding-container">
      <h1 class="product-name">Superhero</h1>
      <p class="product-price">price: <span>500$</span></p>
    </div>
</template>

<script>
export default {
  name: 'ProductPage',
  props: {
    msg: String
  }
}
</script>

<style>
  .product-padding-container {
    padding: 0 auto;
  }
  .product-name {
    margin-bottom: 10px;
    text-align: center;
  }
  .product-price {
    text-align: center;
  }
</style>
