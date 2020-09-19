<template>
  <div id="app">
    <Navbar v-if="window.width > 700"/>
    <Mobilenavbar v-if="window.width<=700"/>
    <Headerimage/>
    <Introtext/>
    <Articles/>
    <Payment/>
    <Map/>
    <Footer/>
    <Sidebar/>
  </div>
</template>

<script>
import Mobilenavbar from './components/mobilenavbar.vue'
import Headerimage from './components/headerimage.vue'
import Introtext from './components/introtext.vue'
import Articles from  './components/articles.vue'
import Payment from './components/payment.vue'
import Sidebar from './components/sidebar.vue'
import Footer from './components/footer.vue'
import Navbar from './components/navbar.vue'
import Map from './components/map'

export default {
  name: 'App',
  components: {
    Mobilenavbar,
    Headerimage,
    Introtext,
    Articles,
    Payment,
    Sidebar,
    Navbar,
    Footer,
    Map,
  },
  data() {
    return {
      window: {
            width: 0,
            height: 0
        }
    }
  },
  created() {
        window.addEventListener('resize', this.handleResize);
        this.handleResize();
    },
    destroyed() {
        window.removeEventListener('resize', this.handleResize);
    },
    methods: {
        handleResize() {
            this.window.width = window.innerWidth;
            this.window.height = window.innerHeight;
        }
    }
  
}
</script>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Open+Sans:wght@300&family=Poppins:wght@300;500&display=swap');

  #app {
    font-family: 'poppins', 'open-sans', sans-serif, Helvetica, Arial;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    margin: 0;
    padding: 0;
    line-height: 30px;
    overflow: auto;
  }

  h1 {
    font-size: 10vmin;
    font-weight: 500;
    line-height: 11vmin;
    padding: 0 20px;
    color: white;
  }

  h2 {
    font-size: 30px;
    font-weight: 500;
    color: white;
  }

  h3 {
    font-size: 37px;
    font-weight: 500;
    line-height: 50px;
    margin-bottom: 30px;
  }

  p {
    font-size: 18px;
    font-weight: 300;
  }

  .margin-100 {
    margin: 100px 0;
  }

  @media only screen and (max-width: 900px) {
    h3 {
      font-size: 35px;
    }
    h2 {
      font-size: 28px;
    }
  }

  @media only screen and (max-width: 700px) {
    
    h2 {
      font-size: 26px;
    }
    h3 {
      font-size: 32px;
    }

    .margin-100 {
      margin: 70px 0;
    }
  }

  @media only screen and (max-width: 500px) {
    
    h2 {
      font-size: 22px;
    }

    h3 {
      font-size: 30px;
    }

    p {
      font-size: 16px;
    }

    .margin-100 {
      margin: 50px 0;
    }
  }

  @media only screen and (max-width: 400px) {
    h2 {
      font-size: 18px;
    }

    h3 {
      font-size: 28px;
    }
  }

</style>
