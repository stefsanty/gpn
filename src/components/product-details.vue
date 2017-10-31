<template>
<div>

    <div class="navbar-placeholder">
        <img src="../../media/banners/3.jpg">
    </div>

    <div class="product-details col-xs-12">
        <div class="product-img-area col-md-5">
            <div class="main-img"><img :src="product.img_link"></div>
            <div class="carousel">Carousel Under Construction</div>
        </div>
        <div class="product-text-area col-md-5">
            <div class="product-name">{{ product.name }}</div>
            <div class="category-box" v-for="category in product.categories" :key="category.id" v-on:click="expandDetails(category)">
                <div :class="category.titleClass">{{ category.title }}</div>
                <div :id="category.textIDSelector" :class="category.textClass">
                    <div v-for="line in category.text.split('\n')">{{ line }}<br></div>
                </div>
            </div>
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
        categories:
        {
          description:
            {
              id: 1,
              titleClass: 'title',
              title: 'Description',
              textClass: 'text hide',
              textIDSelector: 'description-text',
              text: `Somebody once told me the world is gonna roll me
                    I ain't the sharpest tool in the shed
                    She was looking kind of dumb with her finger and her thumb
                    In the shape of an "L" on her forehead
                    
                    Well the years start coming and they don't stop coming
                    Fed to the rules and I hit the ground running
                    Didn't make sense not to live for fun
                    Your brain gets smart but your head gets dumb
                    So much to do, so much to see
                    So what's wrong with taking the back streets?
                    You'll never know if you don't go
                    You'll never shine if you don't glow`
            },
          specifications:
            {
              id: 2,
              titleClass: 'title',
              title: 'Specifications',
              textClass: 'text hide',
              textIDSelector: 'specification-text',
              text: `Height: 69 meters
                    Width: 44 meters
                    Weight: 100 kilograms
                    Niceness: Yes`
            }
        }
        
      }
    }
  },
  methods: {
    expandDetails: function (category) {
      var id = category.textIDSelector
      console.log(category.textIDSelector)
      var element = document.getElementById(id)
      element.classList.toggle('hide')
    }
  }
}
</script>

<style>

.navbar-placeholder {
    height: 110px;
    margin-bottom: 20px;
    overflow: hidden;
}

.product-details {
    padding: 0px;
}

.product-img-area {
    float: left;
    margin-left: 100px;
    padding: 0px;
}

.product-text-area {
    margin-left: 100px;
}

.product-name {
    position: relative;
    left: -30px;
    padding: 10px;
    font-family: 'Geomanist';
    font-size: 3em;
    line-height: 1em;
    background-color: #aaaaff;
    color: white;
    font-weight: 900;
    box-shadow: 4px 2px 2px rgba(33,33,33,0.4);

    margin-bottom: 10px;
}

.category-box {
    margin-bottom: 20px;
}

.title {
    position: relative;
    left: -30px;
    padding: 10px;
    background-color: rgba(100,100,100,0.3);
    font-size: 2em;
    box-shadow: 4px 2px 2px rgba(33,33,33,0.4);
    line-height: 1em;

    margin-bottom: 20px;
}

.text {
    font-size: 1.2em;
}

.main-img>img {
    width: 100%;
}

.hide {
    display: none;
}

</style>
