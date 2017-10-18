<template>
    <div id="banner" class="col-xs-12">
        <main class="gpn-main-text col-xs-12">
            <div class="gpn-text">Our Products</div>
        </main>
        <div class="banner-img-wrapper">
            <img class="banner-img" v-bind:src="banner_img.link" v-bind:alt="banner_img.alt">
        </div>
    </div>
</template>

<script>
window.onload = function () {
  console.log('test')
}

export default {
  name: '#banner',
  data () {
    return {
      banner_img:
        {
          link: require('../../media/banners/2.jpg'),
          alt: 'Luxury in Freedom'
        }
    }
  }
}
</script>



<style scoped>

#banner {
    position: relative;
    margin-bottom: 2em;
    padding: 0em;
    height: 40vh;
    overflow: hidden;

    background-color: #000;
}

#banner>.gpn-main-text {
    position: absolute;
    z-index: 1;

    margin-top: 10vh;
    padding: 0px;
    margin-left: 8vw;

    float: left;
    font-size: 120px;
    font-family: 'Geomanist';
    font-weight: 900;
    color: white;
    padding: 60px 5vw;
    line-height: 1em;
    
}

#banner>.gpn-main-text>.gpn-subtext {
    color: #3333ff;
    font-family: 'Geomanist';
    font-weight: 300;
}

img.banner-img {
    position: relative;
    z-index: 0;

    width: 120%;
    opacity: 0.8;
    height: auto;

}

/* The following 'alters' base.vue's CSS */

.nav-products-box {
    background: rgba(33,33,33,0.6);
    color: #dea988;
    top: -1px;
}

</style>

