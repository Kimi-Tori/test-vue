<template>
  <div class="container">
    <ProductPage/>
    <TabsComponent/>
    <SliderComponent>
      :slider_data='sliderItems'
    </SliderComponent>
    <FormComponent/>
  </div>
</template>

<script>
import ProductPage from './components/ProductPage.vue'
import TabsComponent from './components/Tabs.vue'
import SliderComponent from './components/Slider.vue'
import FormComponent from './components/Form.vue'

export default {
  name: 'App',
  components: {
    ProductPage,
    TabsComponent,
    SliderComponent,
    FormComponent
  },
  data() {
    return {
      sliderItems: [
        { id: 1, name: 'img1', img: '1.jpg'},
        { id: 2, name: 'img2', img: '2.jpg'},
        { id: 3, name: 'img3', img: '3.jpg'},
        { id: 4, name: 'img4', img: '4.jpg'},
        { id: 5, name: 'img5', img: '5.jpg'}
      ]
    }
  }
}
</script>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;600&display=swap');

  body {
    margin: 0;
    padding: 0;
    font-size: 18px;
    font-weight: 400;
    background: #343F4F;
    color: #fff;
    font-family: Montserrat, sans-serif;
    text-transform: none;
  }
  p, a, h1, h2, h3, h4, h5, h6 {
    text-transform: none;
    padding: 0;
    margin: 0;
  }
  .container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 10px;
  }
</style>
