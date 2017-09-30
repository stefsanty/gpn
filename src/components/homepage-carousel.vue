<template>
    <div class="carousel col-xs-12">
        <carousel :scrollPerPage="true" :perPage="4" :loop="true">
            <slide class="carousel-slide" v-for="p in carousel_products" :key="p.id">
                <img class="carousel-img" v-bind:src="p.img_link" v-bind:alt="p.name" v-bind:obj="p" v-on:click="getCarouselDetails()">
            </slide>
        </carousel>
        <div class="carousel-slide-details" style="display: none;">
            
        </div>
   </div>
</template>

<script>
import { Carousel, Slide } from 'vue-carousel'
export default {
  components: {
    Carousel,
    Slide
  },
  name: '.carousel',
  data () {
    return {
      carousel_products:
        {
          p1:
            {
              name: 'Corradi Condominium Special',
              brand: 'Corradi',
              img_link: require('../../media/products/corradi_test.jpg'),
              description: 'Paragraph 1: A favorite of sex fiends and old men. <br />Paragraph 2: Buy it now or else!'
            },
          p2:
            {
              name: 'Corradi again',
              brand: 'Corradi',
              img_link: require('../../media/banners/1.jpg'),
              description: 'This is a banner'
            },
          p3:
            {
              name: 'Corradi again',
              brand: 'Corradi',
              img_link: require('../../media/banners/1.jpg'),
              description: 'This is a banner'
            },
          p4:
            {
              name: 'Corradi again',
              brand: 'Corradi',
              img_link: require('../../media/banners/1.jpg'),
              description: 'This is a banner'
            },
          p5:
            {
              name: 'Corradi again',
              brand: 'Corradi',
              img_link: require('../../media/banners/1.jpg'),
              description: 'This is a banner'
            }
        }
    }
  },
  methods: {
    getCarouselDetails: function () {
      console.log(this._data.carousel_products.p1.name)
      // This should log "Corradi Condominium" or something
    }
  }
}
</script>

<style scoped>

.carousel {
    padding: 0px 7vw;
}

.carousel-slide {
    position: relative;
    border: thin solid black;
    margin: 1vh 1vw;
    height: 21vh;
    overflow: hidden;
}

.carousel-slide>img {
    width: 100%;
}
.carousel-slide>img:hover {
    cursor: pointer;
}

</style>

