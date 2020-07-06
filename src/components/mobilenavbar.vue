<template>
    <div
      class="navbar"
      :class="{ 'navbar--hidden': !showNavbar, 'pastHeader': pastHeader }"
    >
        <img class="svg" src="../assets/menu.svg" alt="" @click="openSidebar">
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
        },
        openSidebar() {
            this.$root.$refs.sidebar.toggleSidebar();
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

    .svg {
        height: 25px;
        width: auto;
        cursor: pointer;
        padding: 15px 15px 0 0;
        filter: invert(100%);
        transition: all .2s ease-in-out; 
    }

    .svg:hover {
        opacity: 0.7;
        transform: scale(1.1);
    }

</style>