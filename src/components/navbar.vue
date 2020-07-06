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
      showSideNavbar: false,
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
        }, 
        setSideNavbar() {
            this.showSideNavbar = !this.showSideNavbar
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
        width: 100%;
        position: fixed;
        transform: translate3d(0, -100%, 0);
        transition: 0.1s all ease-out;
        z-index: 100;
        display: flex;
        justify-content: flex-end;
    }

    .navbar.navbar--visable {
        transform: translate3d(0, -100%, 0);
    }

    .mobileNavbar {
        display: none;
    }

    .pastHeader {
        background-color: #f6b8b6;
        box-shadow: 0 2px 15px rgba(71, 120, 120, 0.5);
    }

    .sideNavbar {
        height: 100%;
        width: 60%;
        min-width: 270px;
        background-color: white;
        position: fixed;
        right: 0;
        transform: translate3d(100%, 0, 0);
        transition: 0.1s all ease-out;
        z-index: 99;
        display: flex;
        flex-direction: column;
        color: black;
    }

    .sideNavbar--visable {
        box-shadow: none;
        transform: translate3d(0, 0, 0);
    }

    .svg {
        filter: invert(100%);
        cursor: pointer;
        text-shadow: 0px 0px 20px rgba(0,0,0,0.3); 
        padding-right: 20px;
    }

    .svg:hover {
        opacity: 0.6;
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

    @media only screen and (max-width: 650px) {
        
        .regularNavbar {
            display: none;
        }

        .mobileNavbar {
            display: flex;
        }

        .p {
            color: black;
        }

  }


</style>