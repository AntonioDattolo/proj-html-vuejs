<script>

export default {
  
  data() {
    return {
        links:{ 
            home :[
            "Main Home",
            "Italian Restaurant",
            "Pizzeria Home",
            "Pizza Light",
            "Pizza Dark",
            "Fast Food Home"],
            pages :[
                "About Us",
                "Our Service",
                "Our Team",
                "Our History",
                "Reservation",
                "Book A Table I",
                "Book A Table II",
                "Contact Us",
                "Get In Touch",
                "Coming Soon",
                "404 Error Page"
            ],
            menu:{
                
                list_types:["Don Peppe Menu","Menu Light","MEnu Filter Light","Menu Dark","Menu Filter Dark","Menu Slider","Restaurant Menu"],
                list_layout:["3 Columns","4 Columns","4 Columns Wide","5 Columns","5 Columns Wide","6 Columns"],
                product_types :["Standard","Grouped","Variable","New","On Sale"],
                shop_pages :["My Account", "Cart", "Checkout"]
            },
            event:["Event List","Event Single"],
            blog: {blog_links:[
                "Right Sidebar",
                "Left Sidebar",
                "Without Sidebar",
                "Post Types"],
                
                    blog_submenu: [ 
                        "Standard",
                        "Gallery",
                        "Quote",
                        "Link",
                        "Audio",
                        "Video",
                        "No Sidebar"

                    ]
                
            },
           
            landing :"Landing",
            logo : "../assets/img/h5-logo-divided-header.png"
            


            }

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
                                <img src="../assets/svg/svg-0.svg" style="height: 5px; filter: invert(1);" alt="">
                                Home
                            </a>
                            <ul class="dropdown-menu" >
                                <li v-for="link in links.home"><a class="text-decoration-none text-black" href="#">{{ link }}</a></li>
                            </ul>
                        </li>
                        <li class=" align-self-center dropdown">
                            <a class="nav-link" href="#">Pages</a>
                            <ul class="dropdown-menu" >
                                <li v-for="link in links.pages"><a class="text-decoration-none text-black" href="#">{{ link }}</a></li>
                            </ul>
                        </li>
                        <li class=" align-self-center dropdown">
                            <a class="nav-link" href="#">Menu</a>
                            <ul class="dropdown-menu" >
                                <li v-for="link in links.menu.list_types"><a class="text-decoration-none text-black" href="#">{{ link }}</a></li>
                            </ul>
                            
                        </li>
                        <li class="">
                            <a class="nav-link active" aria-current="page" href="#">
                                <img src="../assets/img/h5-logo-divided-header.png" style="height: 105px;" alt="">
                            </a>
                        </li>
                        <li class=" align-self-center dropdown">
                            <a class="nav-link active" aria-current="page" href="#">Event</a>
                            <ul class="dropdown-menu" >
                                <li v-for="link in links.event"><a class="text-decoration-none text-black" href="#">{{ link }}</a></li>
                            </ul>
                        </li>
                        <li class=" align-self-center dropdown">
                            <a class="nav-link" href="#">Blog</a>
                            <ul class="dropdown-menu" id="blog-menu" >
                                <li v-for="link,i in links.blog.blog_links">
                                    <a  class="text-decoration-none text-black" href="#">{{ link }}</a>
                                </li>
                            </ul>
                        </li>
                        <li class=" align-self-center">
                            <a class="nav-link" href="#">{{links.landing}}</a>
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
}.dropdown:hover>.dropdown-menu{
    display: block;
    position: absolute;
    left: 0px;
}
#blog-menu>li:last-child::before{
    content: 'baffo';
}
</style>
