<script>
import myData from '../store/data';
import LinkCard from './LinkCard.vue';
import submenu from './submenu.vue'
import imgUrl from '../assets/img/h5-logo-divided-header.png'
import iconUrl from '../assets/svg/svg-0.svg'

export default {
    components :{
    LinkCard,
    submenu
    },
  data() {
   
    return {
        myData,
        imgUrl,
        iconUrl

    }
  },
  methods: {
  
  },
  mounted() {

  }
}

</script>

<template>
    <section class="debug container align-items-center">
        <nav class="bg-transparent">
            <div class="d-flex align-items-center p-2 ">
                <div class="col-2">
                    <button class="btn" style="background-color: #c83b1a; text-wrap: nowrap;">
                        ORDER ONLINE
                    </button>
                </div>
                <div class="col-8">
                    <ul class=" col-12 d-flex justify-content-around m-0" style="list-style: none;">
                        <li class=" align-self-center dropdown">
                            <a class="nav-link" aria-current="page" href="#">
                                <img :src="iconUrl" style="height: 5px; filter: invert(1);" alt="">
                                Home
                            </a>
                            <!-- <ul class="dropdown-menu" >
                                <li v-for="link in links.home"><a class="text-decoration-none text-black" href="#">{{ link }}</a></li>
                            </ul> -->
                            <ul class="dropdown-menu text-start">
                                 <LinkCard v-for="link,i of myData.links.home" :links="link" :index="i"/> 
                            </ul>
                        </li>
                        <li class=" align-self-center dropdown">
                            <a class="nav-link" href="#">Pages</a>
                            <ul class="dropdown-menu" >
                                <LinkCard v-for="link in myData.links.pages" :links="link"/>
                            </ul>
                        </li>
                        <li class=" align-self-center dropdown">
                            <a class="nav-link" href="#">Menu</a>
                            <ul class="dropdown-menu" >
                                <LinkCard v-for="link in myData.links.menu.list_types" :links="link"/>
                            </ul>
                            
                        </li>
                        <li class="">
                            <a class="nav-link active" aria-current="page" href="#">
                                <img :src="imgUrl" style="height: 105px;" alt="">
                            </a>
                        </li>
                        <li class=" align-self-center dropdown">
                            <a class="nav-link active" aria-current="page" href="#">Event</a>
                            <ul class="dropdown-menu" >
                                <LinkCard v-for="link in myData.links.event" :links="link" />
                            </ul>
                        </li>
                        <li class=" align-self-center dropdown">
                            <a class="nav-link" href="#">Blog</a>
                            <ul class="dropdown-menu" id="blog-menu" >
                                <LinkCard v-for="link in myData.links.blog[0].name" :links="link" />
                                <li class="dropdown-item dropdown" style="">
                                    <img style="height: 10px;" class="myVisible" :src="iconUrl" alt="">
                                    <a id="a" class="text-decoration-none text-black" href="#">

                                        {{ myData.links.blog[1].name }}
                                    </a>
                                    <submenu />
                                </li>
                            </ul>
                        </li>
                        <li class=" align-self-center">
                            <a class="nav-link" href="#">{{myData.links.landing}}</a>
                        </li>
                    </ul>
                </div>
                <div class="align-self-center d-flex justify-content-around col-2">
                    <a class="text-decoration-none text-white" href="">CART</a>
                    <a class="text-decoration-none text-white" href="">SEARCH</a>
                </div>
            </div>
        </nav>
    </section>
</template>

<style scoped>
.debug{
    border: 1px solid red;

}.pok{
    position: relative;
}
.dropdown-menu{
    display: none;
    background-color: whitesmoke;
    text-decoration: none;
    list-style: none;
  line-height-step: 0;
    margin-left: 0;
}
.dropdown:hover>.dropdown-menu{
    background-color: rgb(36, 36, 36);
    display: block;
    position: absolute;
    width: 180px;
    left: 0;
}
section{
    margin: 0 auto;
    position: absolute;
    top:0;
    left:15%;
    z-index:1;
}
.myVisible{
  visibility: hidden;
}
.dropdown-item:hover{
  background-color: rgb(92, 91, 91);
  .myVisible{
    visibility: visible;
  }
}
</style>
