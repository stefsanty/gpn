<template>
<!-- contains header navbar and footer -->
<div class="base col-xs-12">

    <div class="navbar">
        <ul>
            <li>
                <router-link to="/" class="nav-home-logo">
                Home<br>
                <img src='../../media/gpn-logo-actual.png'>
                </router-link>
            </li>
            <li>
                <router-link to="/products">
                <div class="nav-text-box" id="nav-products-box">
                        <span>Products</span>
                </div>
                </router-link>
            </li>
            <li>
                <router-link to="/products2">
                <div class="nav-text-box" id="nav-media-box">
                    <span>Products</span>
                </div>
                </router-link>
            </li>
            <li>
                <router-link to="/blog">
                <div class="nav-text-box" id="nav-blog-box">
                <span>Blog</span>
                </div>
                </router-link>
            </li>
        </ul>
    </div>  

    <div class="body">
        <transition name="fade" mode="out-in">
        <router-view name="a"></router-view>
        </transition>
        <transition name="fade" mode="out-in">
        <router-view name="b"></router-view>
        </transition>
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
    src: local('Oxygen'), url(/fonts/Oxygen-Regular.f9ff876.ttf) format('truetype');
}
@font-face {
    font-family: 'Halo';
    src: local('Halo'), url(/fonts/Halo.fa7c9c7.otf) format('opentype');
}
@font-face {
    font-family: 'OneDay';
    src: local('OneDay'), url(/fonts/OneDay.d7a8613.otf) format('opentype');
}
@font-face {
    font-family: 'Geomanist';
    src: local('Geomanist'), url(/fonts/Geomanist.7da2010.ttf) format('truetype');
}
.base {
    font-family: 'Oxygen';
    padding: 0px;
}
.navbar {
    position: fixed;
    width: 100%;
    height: 100px;
    z-index: 3;

    color: white;
    background: rgba(0,0,0,0);
    border-radius: 0px;

    padding: 0px 40px;
    margin: 0px 100px;
}
.navbar>ul {
    list-style-type: none;
    margin: 0px;
    padding: 0px;
}
.navbar>ul>li {
    float: left;

    font-size: 20px;
    text-align: center;
    
    margin: 0em 1vw;
}
.navbar>ul>li>router-link {
    color: white;
}

.navbar>ul>li>a:hover {
    text-decoration: none;
}

.navbar>ul>li>a {
    text-decoration: none;
    background: rgba(33,33,233,0.8);
}

.nav-text-box {
    position: relative;
    top: -30px;
    width: 160px;
    height: 130px;

    color: white;
    padding: 2em;
    background: rgba(0,0,0,0.25);
    box-shadow: 1px 1px 1px rgba(0,0,0,0);
    transition: color 0.2s, background 0.3s, top 0.3s;
}
.nav-text-box>span {
    position: relative;
    top: 30px;
}

.nav-text-box:hover {
    background: rgba(33,33,33,0.6);
    color: #dea988;
    top: -1px;
}
.nav-text-box:enabled {
    background: rgba(33,33,33,0.8);
    color: #dea988;
    top: -1px;
}

.nav-home-logo {
    display: inline-block;
    position: relative;
    top: -30px;
    
    text-align: center;
    color: white;

    padding: 0px;
    margin-right: 40px;
    height: 100px;
    transition: color 0.2s, background 0.3s, top 0.3s;
}

.nav-home-logo:hover {
    color: white;
    top: 10px;
}

.nav-home-logo>img {
    width: auto;
    max-height: 100%;
}

.fade-enter-active, .fade-leave-active {
  transition: opacity 0.7s ease
}
.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
}

.fade-v-enter-to, .fade-v-leave {
  opacity: 1;
}

</style>