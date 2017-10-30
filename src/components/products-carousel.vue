<template>
    <div class="carousel col-xs-12">
        <carousel :scrollPerPage="true" :perPage="4" :loop="true">
            <slide class="carousel-slide" v-for="product in carousel_products" :key="product.id">
                <img class="carousel-img" v-bind:src="product.img_link" v-bind:alt="product.name" v-on:click="getCarouselDetails(product)">
            </slide>
        </carousel>
        <div id="details" :style="details.style"> 
          <div class="details-img"><img v-bind:src="details.img_link"></div>
          <div class="details-name">{{ details.name }}</div>
          <div class="details-description" v-html="details.description"></div>
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
        [
          {
            id: 1,
            name: 'Corradi Condominium',
            brand: 'Corradi',
            img_link: require('../../media/products/corradi_test.jpg'),
            description: 'Somebody once told me the world is gonna roll me'
          },
          {
            id: 2,
            name: 'Corradi again',
            brand: 'Corradi',
            img_link: require('../../media/banners/1.jpg'),
            description: 'I ain\'t the sharpest tool in the shed'
          },
          {
            id: 3,
            name: 'Corradi again',
            brand: 'Corradi',
            img_link: require('../../media/banners/3.jpg'),
            description: 'She was looking kind of dumb with her finger and her thumb'
          },
          {
            id: 4,
            name: 'Corradi again',
            brand: 'Corradi',
            img_link: require('../../media/banners/3.jpg'),
            description: 'In the shape of an "L" on her forehead'
          },
          {
            id: 5,
            name: 'Corradi again',
            brand: 'Corradi',
            img_link: require('../../media/banners/1.jpg'),
            description: `Well the years start coming and they don't stop coming
                          Fed to the rules and I hit the ground running
                          Didn't make sense not to live for fun
                          Your brain gets smart but your head gets dumb
                          So much to do, so much to see
                          So what's wrong with taking the back streets?
                          You'll never know if you don't go
                          You'll never shine if you don't glow`
          }
        ],
      details: {
        img_link: '',
        name: '',
        description: '',
        style: { display: 'none' }
      }
    }
  },
  methods: {
    getCarouselDetails: function (product) {
      var details = this.details

      // Animate closing details div if not hidden

      // Populate and show details div
      details.img_link = product.img_link
      details.name = product.name
      details.description = product.description
      details.style = { animation: 'fadein 1s' }
      details.description = details.description.replace(/\n/g, '<br />')

      // // Specify location of link and div
      // let d = document
      // let detailsAnchor = d.getElementById('details') // there is only 1
      // let linksToDetailsAnchor = d.getElementsByClassName('carousel-img')
      // // linksToDeatilsAnchor contains all carousel-img's

      // // pure JS scroll
      // //   ############ Insert pure JS scroll here ############
      // //   ############ Insert pure JS scroll here ############
      // //   ############ Insert pure JS scroll here ############

      // // addEventListener to each carousel-img
      // for (let i = 0; i < linksToDetailsAnchor.length; i++) {
      //   linksToDetailsAnchor[i].addEventListener('click', scrollTo(detailsAnchor, 0, 1250), false)
      // }
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

.details-img {
  width: 100%;
}

.details-img>img {
    width: 100%;
}

@keyframes fadein {
    from { opacity: 0; }
    to   { opacity: 1; }
}


</style>

