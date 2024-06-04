<script>

import myData from '../store/data';
import background from '../assets/img/cielostellato.png'
import slideBg_1 from '../assets/img/h3-rev-img-1.png'
import slideBg_2 from '../assets/img/h3-rev-img-3.png'
import slideBg_3 from '../assets/img/h3-rev-img-5.png'
import slide_1 from '../assets/img/h3-rev-img-2.png'
import slide_2 from '../assets/img/h3-rev-img-4.png'
import slide_3 from '../assets/img/h3-rev-img-6.png'

export default {
  components: {
   
  },
  data() {
    return {
      myData,
      background,
      carousel_slide:[
        slide_1,
        slide_2,
        slide_3
      ],
      carousel_bg:[
      slideBg_1,
        slideBg_2,
        slideBg_3,
      ]

    }
  },
  methods: {
  
  },
  mounted() {

  }
}


</script>

<template>
  <!-- impostare una variabile per swichtare le slide del carosello -->
    <section class="d-flex justify-content-center align-items-center flex-wrap debug" v-bind:style="{ backgroundImage: 'url(' + background + ')' }">
     <div class="p-5" style=" border: 1px solid red;">
        <img :src="carousel_slide[0]" alt="">
        <img style="position: absolute;left:30%;z-index:-2;top:30%" :src="carousel_bg[0]" alt="">
     </div>
    </section>
  
</template>

<style scoped>
.myBg{
  position: absolute;
  top:-150px;
  z-index: -1;
  object-fit: contain;
  object-position: bottom;
  height: 750px;
  width: 100%; 
} 
section{
  position: absolute;
  top :-25px;
  z-index: -1;
  height: 80vh;
  width: 100%;
  background-repeat: no-repeat;
  background-size: cover;
  background-position: bottom;
  padding-top:10rem ;
}
.carousel{

}

</style>