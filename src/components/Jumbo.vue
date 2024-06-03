<script>




export default {
  components: {
   
  },
  data() {
    return {
      background: "../assets/img/cielostellato.PNG"

    }
  },
  methods: {
  
  },
  mounted() {

  }
}


</script>

<template>
    <section style="width: 100%;" >
       <img class="w-100" src="../assets/img/cielostellato.PNG" alt="">
    </section>
  
</template>

<style scoped>
img{
  position: absolute;
  top:-150px;
  z-index: -1;
  object-fit: contain;
  object-position: bottom;
  height: 750px; 
}

</style>