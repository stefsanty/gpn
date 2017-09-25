<template>
    <div class="carousel col-xs-12">
        <carousel :scrollPerPage="true" :perPage="4">
            <slide>
                <div>Pirates in gay space</div>
                <div>Pirates in gay space</div>
                <div>Pirates in gay space</div>
            </slide>
            <slide>
                <div>Bushido practice of the Blue Moon</div>
                <div>Bushido practice of the Blue Moon</div>
            </slide>
            <slide>
                <div>Kenny Rogers giving Benjamin Franklin a rimjob</div>
                <div>Kenny Rogers giving Benjamin Franklin a rimjob</div>
                <div>Kenny Rogers giving Benjamin Franklin a rimjob</div>
                <div>Kenny Rogers giving Benjamin Franklin a rimjob</div>
            </slide>
            <slide>
                <div>Empty rambunctious fruit salad toupee</div>
                <div>Empty rambunctious fruit salad toupee</div>
            </slide>
            <slide>
                <div>Empty rambunctious fruit salad toupee</div>
                <div>Empty rambunctious fruit salad toupee</div>
            </slide>
            <slide>
                <div>Empty rambunctious fruit salad toupee</div>
                <div>Empty rambunctious fruit salad toupee</div>
            </slide>
        </carousel>
   </div>
</template>

<script>
import { Carousel, Slide } from 'vue-carousel'
export default {
  components: {
    Carousel,
    Slide
  }
}
</script>

<style scoped>

.carousel {
    padding: 0px 10vw;
}

</style>

