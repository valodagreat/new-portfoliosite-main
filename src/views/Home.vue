<template>
  <div class="home">
    <Particles
      id="tsparticles"
      class="particles"
      :options="{
            background: {
                color: {
                    value: '#007bff'
                }
            },
            fpsLimit: 60,
            interactivity: {
                detectsOn: 'canvas',
                events: {
                    onClick: {
                        enable: true,
                        mode: 'push'
                    },
                    onHover: {
                        enable: true,
                        mode: 'repulse'
                    },
                    resize: true
                },
                modes: {
                    bubble: {
                        distance: 400,
                        duration: 2,
                        opacity: 0.8,
                        size: 40
                    },
                    push: {
                        quantity: 4
                    },
                    repulse: {
                        distance: 200,
                        duration: 0.4
                    }
                }
            },
            particles: {
                color: {
                    value: '#ffffff'
                },
                links: {
                    color: '#ffffff',
                    distance: 150,
                    enable: true,
                    opacity: 0.5,
                    width: 1
                },
                collisions: {
                    enable: true
                },
                move: {
                    direction: 'none',
                    enable: true,
                    outMode: 'bounce',
                    random: false,
                    speed: 6,
                    straight: false
                },
                number: {
                    density: {
                        enable: true,
                        value_area: 800
                    },
                    value: 80
                },
                opacity: {
                    value: 0.5
                },
                shape: {
                    type: 'circle'
                },
                size: {
                    random: true,
                    value: 5
                }
            },
            detectRetina: true
        }"
    />
    <div class="home-container">
      <div class="inner-container">
        <div class="pl-2">
          <b-avatar  src="https://res.cloudinary.com/valodagreat/image/upload/v1606254253/caleb_r40hjv.jpg" :size="size"></b-avatar>
        </div>
        <div class="intro">
          <h1 >Hi There!</h1>
          <h3>I'm Valentine,a fullstack web developer <b-icon icon="laptop" animation="fade" font-scale="1.2"></b-icon></h3>
          <span class="p-2">
            <span class="pr-2">
              <b-button class="btnn" pill variant="light">
                <router-link to="/about">About me</router-link>
              </b-button>
            </span>
          <b-button class="btnn" pill variant="light">
            <router-link to="/portfolio">Portfolio</router-link>
          </b-button>
        </span>
        </div>
      </div>
    </div>
    <div class="intro p-1">
      <h3 class="text-center">Services</h3>
        <div class="carousel-wrappers mx-auto">
          <VueSlickCarousel v-bind="settings">
            <div class="carouselslide">
              <div class="px-5">
                <b-avatar  src="https://res.cloudinary.com/valodagreat/image/upload/v1606381767/undraw_design_community_rcft_w2ijz8.png" size="8rem"></b-avatar>
              </div>
              <h4 class="py-2 pl-2">Design and Development</h4>
              <p class="pl-2">Develop and Design applications <br/><span class="px-3"> from foundational level</span> <br/><span class="px-3"> to full production level</span></p>
            </div>
            <div class="carouselslide">
            <div class="px-5">
              <b-avatar  src="https://res.cloudinary.com/valodagreat/image/upload/v1606378065/undraw_segment_analysis_bdn4_komzqp.png" size="8rem"></b-avatar>
            </div>
            <h4 class="py-2 pl-2">Analytics</h4>
            <p class="pl-2">Get insights into who browses your site <br/><span class="px-3"> in order to make smarter</span> <br/><span class="px-3"> business decisions</span></p>
          </div>
          <div class="carouselslide">
            <div class="px-5">
              <b-avatar  src="https://res.cloudinary.com/valodagreat/image/upload/v1606378064/audit_tsetrf.png" size="8rem"></b-avatar>
            </div>
            <h4 class="py-2 pl-2">Website Audits</h4>
            <p class="pl-2">Looking to improve your page  <br/><span class="px-3">performance,SEO, or user experience?</span> <br/><span class="px-3"> Contact me</span></p>
          </div>
          <div class="carouselslide">
            <div class="px-5">
              <b-avatar  src="https://res.cloudinary.com/valodagreat/image/upload/v1606378064/undraw_mobile_prle_gzgpfx.png" size="8rem"></b-avatar>
            </div>
            <h4 class="py-2 pl-2">Mobile Friendly</h4>
            <p class="pl-2">Create highly responsive and <br/><span class="px-3">scalable web applications</span> <br/><span class="px-3"> for client's use</span></p>
          </div>
          <div class="carouselslide">
            <div class="px-5">
              <b-avatar  src="https://res.cloudinary.com/valodagreat/image/upload/v1606378413/undraw_Add_content_re_vgqa_uj3fys.png" size="8rem"></b-avatar>
            </div>
            <h4 class="py-2 pl-2">Content Management</h4>
            <p class="pl-2">Creating and managing content<br/><span class="px-3">as in blog posts e.t.c .</span> </p>
          </div>
          </VueSlickCarousel>
        </div>
    </div>
    <div class="my-5 py-5" >
      <hr class="hlr">
    </div>
    <Footer />
  </div>
</template>

<script>
// @ is an alias to /src
import VueSlickCarousel from 'vue-slick-carousel'
import Footer from '../components/HelloWorld'
import 'vue-slick-carousel/dist/vue-slick-carousel.css'
  // optional style for arrows & dots
import 'vue-slick-carousel/dist/vue-slick-carousel-theme.css'

export default {
  name: 'Home',
  components: {
    VueSlickCarousel,
    Footer
  },
  data() {
    return {
      screen : screen.width,
      size : '',
      settings: {
        "dots": true,
        "infinite": true,
        "speed": 500,
        "slidesToShow": 3,
        "slidesToScroll": 1,
        "initialSlide": 0,
        "swipeToSlide": true,
        "autoplay": true,
        //"autoplaySpeed": 3000,
        "responsive": [
        {
          "breakpoint": 1024,
          "settings": {
            "slidesToShow": 2,
            "slidesToScroll": 1,
            "infinite": true,
            "dots": true
          }
        },
        {
          "breakpoint": 600,
          "settings": {
            "slidesToShow": 1,
            "slidesToScroll": 1,
            "initialSlide": 2
          }
        },
        {
          "breakpoint": 480,
          "settings": {
            "slidesToShow": 1,
            "slidesToScroll": 1
      }
    }
  ]
}
    }
  },
  mounted(){
    this.screen = screen.width
    this.getSize()
  },
  methods: {
    getSize(){
      if(this.screen > 768){
        this.size= '15rem'
      }else{
        this.size= '7rem'
      }
    }
  }
}
</script>

<style >
  /*.home{
    background: rgb(102,16,242);
    background: linear-gradient(0deg, rgba(102,16,242,1) 9%, rgba(91,67,214,1) 29%, rgba(0,123,255,1) 67%);
  }*/
  .particles{
    position: fixed;
    height: 100%;
    width: 100%;
    z-index: -1;
  }
  .home-container{
    display: grid;
    place-items: center;
    height: 100vh;
  }
  .inner-container{
    display: flex;
    justify-content: space-between !important;
    align-items: center;
  }
  .intro{
    color: white;
    padding: 2rem;
  }
  .btnn a{
    color: #212529;
  }
  .btnn a:hover{
    text-decoration: none;
    color: #212529;
  }
  .carousel-wrappers{
    max-width: 80vw !important;
    text-align: center;
  }
  hr.hlr{
    border: 2px solid white;
    width: 70vw ;
  }
  @media screen and (max-width:768px){
    .inner-container{
    display: flex;
    flex-direction: column;
    justify-content: space-between !important;
    align-items: center;
  }
  .intro{
    text-align: center;
  }
  }
</style>