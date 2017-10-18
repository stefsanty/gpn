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
                <router-link to="/products" class="nav-option">
                <div class="nav-text-box">
                        <span class="nav-text">Products</span>
                </div>
                </router-link>
            </li>
            <li>
                <router-link to="/media" class="nav-option">
                <div class="nav-text-box">
                    <span class="nav-text">Media</span>
                </div>
                </router-link>
            </li>
            <li>
                <router-link to="/blog" class="nav-option">
                <div class="nav-text-box">
                <span class="nav-text">Blog</span>
                </div>
                </router-link>
            </li>
        </ul>
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
    overflow: hidden;
}
.navbar {
    position: absolute;
    width: 100%;
    height: 100px;
    z-index: 1;

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

.nav-text-box {
    position: relative;
    top: -40px;
    width: 160px;
    height: 160px;

    color: white;
    padding: 2em;
    background: rgba(0,0,0,0.3);
    transition-timing-function: linear;
    transition: color 0.3s, background 0.5s, top 1s;
}
.nav-text-box>.nav-text {
    position: relative;
    top: 40px;
}

.nav-text-box:hover {
    background: rgba(33,33,33,0.6);
    color: #dea988;
    top: 0px;
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

    transition-timing-function: linear;
    transition: color 0.3s, background 0.5s, top 1s;
}

.nav-home-logo:hover {
    color: #dea988;
    top: 0px;
}

.nav-home-logo>img {
    width: auto;
    max-height: 100%;
}

</style>