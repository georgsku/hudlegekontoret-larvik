<template>
    <div
      class="navbar"
      :class="{ 'navbar--hidden': !showNavbar, 'pastHeader': pastHeader }"
    >
        <p @click="navbarClick('introtext')">Om oss</p>
        <p @click="navbarClick('timebestillinger')">Timebestillinger</p>
        <p @click="navbarClick('åpningstimer')">Åpningstider</p>
        <p @click="navbarClick('lysbehandling')">Lysbehandling</p>
        <p @click="navbarClick('betaling')">Betaling</p>
        <p @click="navbarClick('googlemaps')">Kart</p>
    </div>
</template>

<script>
export default {
  data () {
    return {
      showNavbar: true,
      pastHeader: false,
      lastScrollPosition: 0
    }
  },
    methods: {
        onScroll () {
            const currentScrollPosition = window.pageYOffset || document.documentElement.scrollTop
            if (currentScrollPosition < 0) {
                return
            }
            if (Math.abs(currentScrollPosition - this.lastScrollPosition) < 60) {
                return
            }
            if (currentScrollPosition > (window.innerHeight * 0.7) ) {
                this.pastHeader = true
            } else {
                this.pastHeader = false
            }
            this.showNavbar = currentScrollPosition < this.lastScrollPosition
            this.lastScrollPosition = currentScrollPosition
        },
        navbarClick(element) {
            document.getElementById(element).scrollIntoView({behavior: "smooth", block: "center",});
        }
    },
    mounted () {
            window.addEventListener('scroll', this.onScroll)
        },
    beforeDestroy () {
        window.removeEventListener('scroll', this.onScroll)
    },
}
</script>

<style scoped>
    
    .navbar {
        height: 60px;
        width: 100vw;
        position: fixed;
        transform: translate3d(0, 0, 0);
        transition: 0.1s all ease-out;
        z-index: 100;
        display: flex;
        justify-content: flex-end;
    }
    .navbar.navbar--hidden {
        box-shadow: none;
        transform: translate3d(0, -100%, 0);
    }

    .pastHeader {
        background-color: #f6b8b6;
        box-shadow: 0 2px 15px rgba(71, 120, 120, 0.5);
    }

    p {
        font-size: 16px;
        font-weight: 400;
        margin: auto 9px;
        color: white;
        cursor: pointer;
        text-shadow: 0px 0px 20px rgba(0,0,0,0.3); 
    }

    p:hover {
        opacity: 0.6;
    }


</style>