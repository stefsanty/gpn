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
          link: require('../../media/banners/3.jpg'),
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
    height: 100vh;
    overflow: hidden;

    background-color: #000;
}

#banner>.gpn-main-text {
    position: absolute;
    line-height: 300px;
    z-index: 1;

    margin-top: 30vh;
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

@keyframes moving-banner-img {
    0%      {transform: translate(-340px, -200px);}
    100%    {transform: translate(0px, 0px); width: 100%;}
}

img.banner-img {
    position: relative;
    z-index: 0;

    width: 120%;
    opacity: 0.6;
    height: auto;

    animation-name: moving-banner-img;
    animation-duration: 40s;
}

</style>

