<template>
<!-- contains header navbar and footer -->
<div class="base col-xs-12">

    <div class="head navbar">
            <router-link to="/" class="nav-home-logo">Home</router-link>
            <router-link to="/products" class="nav-option">Products</router-link>
            <router-link to="/media" class="nav-option">Media</router-link>
            <router-link to="/blog" class="nav-option">Blog</router-link>
    </div>

    <div class="body">
        <router-view name="a"></router-view>
        <router-view name="b"></router-view>
        <router-view name="c"></router-view>
    </div>
    
</div>

</template>

<script>
export default {
  name: 'base',
  components: {
  },
  data () {
    return {

    }
  },

  computed: {},
  methods: {},
  mounted () {}
}
</script>

<style>

@font-face {
    font-family: 'Oxygen';
    src: local('Oxygen'), url(../../static/fonts/Oxygen/Oxygen-Regular.ttf) format('truetype');
}

@font-face {
    font-family: 'Halo';
    src: local('Halo'), url(../../static/fonts/Halo/Halo.otf) format('opentype');
}

@font-face {
    font-family: 'OneDay';
    src: local('OneDay'), url(../../static/fonts/OneDay/OneDay.otf) format('opentype');
}

@font-face {
    font-family: 'Geomanist';
    src: local('Geomanist'), url(../../static/fonts/Geomanist/Geomanist.ttf) format('truetype');
}

.base {
    font-family: 'Oxygen';
    padding: 0px;
}

.head {
    color: white;
    background-color: black;
    border: 0px;
}

.navbar {
    border-radius: 0px;
    padding: 2em;
    margin: 0px;
}

</style>