<template>
  <div id="app">
    <Headerimage/>
    <Introtext/>
    <Articles/>
    <Map/>
    <Footer/>
  </div>
</template>

<script>
import Headerimage from './components/headerimage.vue'
import Introtext from './components/introtext.vue'
import Articles from  './components/articles.vue'
import Footer from './components/footer.vue'
import Map from './components/map'

export default {
  name: 'App',
  components: {
    Headerimage,
    Introtext,
    Articles,
    Footer,
    Map,
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
  }

  h1 {
    font-size: 72px;
    font-weight: 500;
    color: white;
  }

  h3 {
    font-size: 38px;
    font-weight: 500;
    margin-bottom: 30px;
  }

  p {
    font-size: 17px;
    font-weight: 300;
  }

  @media only screen and (max-width: 700px) {
  h1 {
    font-size: 50px;
    }
  }
  @media only screen and (max-width: 400px) {
  h1 {
    font-size: 30px;
    }
  }

</style>
