<template>
    <div id="banner" class="col-xs-12">
        <main class="gpn-main-text col-xs-12">
            <div class="gpn-text">Gaya Prima Nirmala</div>
            <div class="gpn-subtext">Freedom In Luxury.</div>
            <div class="gpn-subtext">FREEDOM IN LUXURY.</div>
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
          link: require('../../media/banner.jpg'),
          alt: 'Luxury in Freedom'
        }
    }
  }
}
</script>

<style scoped>

#banner {
    position: relative;
    border: thin solid black;
    margin-bottom: 2em;
    padding: 0em;
    height: 500px;
    overflow:hidden;
}

#banner>.gpn-main-text {
    position: absolute;
    z-index: 1;

    font-size: 90px;
    font-weight: 900;
    color: black;
    padding: 60px 5vw;
    line-height: 1em;
    
    display: inline;
}

#banner>.gpn-main-text>.gpn-subtext {
    color: #111155;
    font-family: 'Geomanist';
    font-weight: 300;
}

@keyframes moving-banner-img {
    0%      {transform: translate(-340px, -600px);}
    100%    {transform: translate(0px, 0px); width: 100%;}
}

img.banner-img {
    position: relative;
    z-index: 0;

    width: 120%;
    background: #333;
    opacity: 0.7;
    height: auto;

    animation-name: moving-banner-img;
    animation-duration: 40s;
}

</style>

