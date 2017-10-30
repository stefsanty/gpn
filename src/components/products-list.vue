<template>
    <div class="col-xs-12">
        
    <div class="products-list">
        <div class="product-box col-xs-12 col-md-4" v-for="product in products" :key="product.id">
            <router-link v-bind:to="'/products2/' + product.id">
                <div class="product-img"><img v-bind:src="product.img_link"></div>
                <div class="product-title">{{ product.name }}</div>
            </router-link>
        </div>
    </div>
    
    </div>
</template>

<script>
export default {
  name: '.carousel',
  data () {
    return {
      products:
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
            name: 'Shooting Star',
            brand: 'Corradi',
            img_link: require('../../media/banners/1.jpg'),
            description: 'I ain\'t the sharpest tool in the shed'
          },
          {
            id: 3,
            name: 'Deuce Bigalow',
            brand: 'Corradi',
            img_link: require('../../media/banners/3.jpg'),
            description: 'She was looking kind of dumb with her finger and her thumb'
          },
          {
            id: 4,
            name: 'Male Gigolo',
            brand: 'Corradi',
            img_link: require('../../media/banners/3.jpg'),
            description: 'In the shape of an "L" on her forehead'
          },
          {
            id: 5,
            name: 'Electric Corradilow',
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
  }
}
</script>

<style scoped>

.products-list {
    padding: 0px 8vw;
}

.product-box {
    padding: 0px 2vw;
    display: flex;
    flex-direction: column;
    overflow: hidden;
    margin-bottom: 2em;
}

.product-box>a:hover {
    text-decoration: none;
}


.product-img {
    display: inline-block;
    height: 320px;
    width: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
}

.product-img>img {
    width: 100%;
    
}

.product-title {
    text-align: center;
    font-size: 1.8em;
    font-weight: 100;
    font-family: 'Oxygen';
    margin-bottom: 10px;
    background-color: white;
    color: grey;
    transition: color 0.5s, background-color 0.5s ease;
}

.product-title:hover, .product-img:hover ~ .product-title {
    color: white;
    background-color: rgba(102,102,255,0.5)
}

.product-description {
    color: black;
    font-size: 1.3em;
    font-family: 'Oxygen';
    line-height: 1.5em;
}

</style>
