<template>
    <div id="banner" class="col-xs-12">
        <main class="gpn-main-text col-xs-12">
            <div class="gpn-text">Gaya Prima Nirmala</div>
            <div class="gpn-subtext">Freedom In Luxury.</div>
            <div class="gpn-subtext" style="display: none;">FREEDOM IN LUXURY.</div>
        </main>
        <div class="banner-img-wrapper">
            <img class="banner-img" v-bind:src="banner_img.link" v-bind:alt="banner_img.alt">
        </div>
    </div>
</template>

<script>
export default {
  name: '#banner',
  data () {
    return {
      banner_img:
        {
          link: require('../../media/banners/1.jpg'),
          alt: 'Luxury in Freedom'
        }
    }
  }
}
</script>



<style scoped>

#banner {
    position: relative;
    border: thin solid #333;
    margin-bottom: 2em;
    padding: 0em;
    height: 40vh;
    overflow: hidden;

    background-color: #000;
}

#banner>.gpn-main-text {
    position: absolute;
    z-index: 1;

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

</style>

