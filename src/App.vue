<template>
  <div id="app">
    <Headerimage/>
    <Introtext/>
    <Articles/>
    <Payment/>
    <Map/>
    <Footer/>
  </div>
</template>

<script>
import Headerimage from './components/headerimage.vue'
import Introtext from './components/introtext.vue'
import Articles from  './components/articles.vue'
import Payment from './components/payment.vue'
import Footer from './components/footer.vue'
import Map from './components/map'

export default {
  name: 'App',
  components: {
    Headerimage,
    Introtext,
    Articles,
    Payment,
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
    overflow: auto;
  }

  h1 {
    font-size: 10vmin;
    font-weight: 500;
    line-height: 90px;
    color: white;
  }

  h3 {
    font-size: 38px;
    font-weight: 500;
    line-height: 50px;
    margin-bottom: 30px;
  }

  p {
    font-size: 18px;
    font-weight: 300;
  }

  @media only screen and (max-width: 900px) {
    h1 {
      line-height: 75px;
      }
    h3 {
      font-size: 36px;
    }
  }

  @media only screen and (max-width: 700px) {
    h1 {
      line-height: 70px;
    }
    h3 {
      font-size: 36px;
    }
  }

  @media only screen and (max-width: 500px) {
    h1 {
      line-height: 53px;
    }

    h3 {
      font-size: 34px;
    }

    p {
      font-size: 16px;
    }
  }

  @media only screen and (max-width: 400px) {
    h1 {
      padding: 0 10px;
    }
    h3 {
      font-size: 32px;
    }
  }

</style>
