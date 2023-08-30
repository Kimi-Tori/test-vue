<template>
    <swiper class="parallax-slider"
    :navigation="{nextEl: '.swiper-button-next', prevEl: '.swiper-button-prev'}"
    >
        <swiper-slide class="parallax-slide" v-for='image in images' :key='image.id'>
            <div class="parallax-slide-image">
                <img :src='image.imageUrl'/>
            </div>
        </swiper-slide>
        <div class="swiper-button-next"></div>
        <div class="swiper-button-prev"></div>
    </swiper>
</template>

<script>
import SwiperCore, { Navigation } from 'swiper'
import {Swiper, SwiperSlide} from 'swiper/vue'
import 'swiper/swiper.scss'
import 'swiper/components/navigation/navigation.scss';
import 'swiper/swiper-bundle.css';

SwiperCore.use([Navigation])

export default {
    name: 'SliderComponent',
    data() {
        return {
            images: [
                {
                    id:1, 
                    imageUrl: require('../assets/images/slide-1.jpg')
                },
                {
                    id:2, 
                    imageUrl: require('../assets/images/slide-2.jpg')
                },
                {
                    id:3, 
                    imageUrl: require('../assets/images/slide-3.jpg')
                },
                {
                    id:4, 
                    imageUrl: require('../assets/images/slide-4.jpg')
                },
                {
                    id:5, 
                    imageUrl: require('../assets/images/slide-5.jpg')
                },
                {
                    id:6, 
                    imageUrl: require('../assets/images/slide-6.jpg')
                }
            ]
        }
    },
    components: {
        Swiper,
        SwiperSlide
    }
}
</script>

<style>
.parallax-slider {
    width: calc(100% + 20px);
    transform: translateX(-10px);
}
.parallax-slide-image img {
    width: 100%;
}
.swiper-button-next, .swiper-button-prev {
  background-color: transparent;
  padding: 0 10px;
}
</style>