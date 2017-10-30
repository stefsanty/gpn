<template>
<div id="b-part">

<div class="b-container">
    <div class="b-textbox">
        <div class="b-title">Furnish your life</div>
        <div class="b-subtitle">Complete your lifestyle experience with world-class designs from the best brands in the world.</div>
    </div>

    <div class="logos col-xs-12">
        <div class="logo-container" v-for="logo in logos" :key="logo.id">
            <div class="img-container">
                <img v-bind:src="logo.img_link">
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
      logos:
        [
          {
            id: 1,
            img_link: require('../../media/logo/corradi.jpg')
          },
          {
            id: 2,
            img_link: require('../../media/logo/national_gypsum.jpg')
          },
          {
            id: 3,
            img_link: require('../../media/logo/diasen.png')
          },
          {
            id: 4,
            img_link: require('../../media/logo/mr_beams.jpg')
          },
          {
            id: 5,
            img_link: require('../../media/logo/ermetika.gif')
          },
          {
            id: 6,
            img_link: require('../../media/logo/renson.jpg')
          },
          {
            id: 7,
            img_link: require('../../media/logo/national_gypsum.jpg')
          },
          {
            id: 8,
            img_link: require('../../media/logo/owarimonogatari.jpg')
          },
          {
            id: 9,
            img_link: require('../../media/logo/diasen.png')
          },
          {
            id: 10,
            img_link: require('../../media/logo/kyoani.png')
          },
          {
            id: 11,
            img_link: require('../../media/logo/corradi.jpg')
          },
          {
            id: 12,
            img_link: require('../../media/logo/ermetika.gif')
          }
        ]
    }
  }
}
</script>

<style scoped>

#b-part {
    display: inline-block;
}

.b-container {
    color: #696999;
    text-align: center;
}

.b-textbox {
    margin-bottom: 20px;
}

.b-title {
    font-size: 80px;
    font-weight: 300;
    font-family: "Geomanist";
    margin: 20px 0px 0px 0px;
}

.b-subtitle {
    font-size: 30px;
    font-weight: 300;
    line-height: 2em;
    font-family: "Geomanist";
}

.logos {
    padding: 0px 7vw;
}

.logo-container {
    display: inline-block;
    position: relative;
    margin: 1vh 1vw;
}

.logo-container>.img-container {
    height: 70px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    margin: 30px 20px;
}

.logo-container>.img-container>img {
    height: 70px;
    width: auto;
}

</style>
