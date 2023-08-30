<template>
    <div class="product-page-img-conteiner">
      <img src='../assets/images/preview.jpg' alt="preview img" class="product-page-img">
    </div>
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
  .product-page-img-conteiner {
    max-width: 1200px;
    width: calc(100% + 20px);
    transform: translateX(-10px);
    margin: 0 auto;
    object-fit: cover;
  }
  .product-page-img {
    width: 100%;
    height: 100%;
  }
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
