<template>
<div>

    <div class="navbar-placeholder">
    </div>

    <div class="product-details">
        <div class="product-img-box">
            <div class="main-img"><img :src="product.img_link"></div>
            <div class="carousel">Carousel Under Construction</div>
        </div>
        <div class="product-text">
            <div class="title">{{ product.name }}</div>
            <div class="description">{{ product.description }}</div>
        </div>
    </div>

</div> 
</template>
<script>
export default {
  data () {
    return {
      product: {
        id: 1,
        name: 'Corradi Condominium',
        brand: 'Corradi',
        img_link: require('../../media/products/corradi_test.jpg'),
        img_link2: require('../../media/banners/1.jpg'),
        img_link3: require('../../media/banners/3.jpg'),
        description: 'Somebody once told me the world is gonna roll me'
      }
    }
  }
}
</script>

<style>

.product-details {
    margin: auto;
    width: 90%;
    padding: 0px;
}

.product-img-box {
    width: 70%;
    padding: 0px;
}

.main-img>img {
    width: 100%;
}
</style>
