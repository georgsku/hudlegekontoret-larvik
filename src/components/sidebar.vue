<template>
    <div class="sidebar">
        <div class="sidebar-backdrop" @click="closeSidebarPanel" v-if="isPanelOpen"></div>
        <transition name="slide">
            <div v-if="isPanelOpen"
                 class="sidebar-panel">
                <div @click="navbarClick('introtext')">Om oss</div>
                <div @click="navbarClick('timebestillinger')">Timebestillinger</div>
                <div @click="navbarClick('åpningstimer')">Åpningstider</div>
                <div @click="navbarClick('lysbehandling')">Lysbehandling</div>
                <div @click="navbarClick('betaling')">Betaling</div>
                <div @click="navbarClick('googlemaps')">Kart</div>
            </div>
        </transition>
    </div>
</template>
<script>
    export default {
        data: () => ({
            isPanelOpen: false
        }),
        created() {
            this.$root.$refs.sidebar = this;
        },
        methods: {
            closeSidebarPanel() {
                this.isPanelOpen = false
            },
            toggleSidebar() {
                this.isPanelOpen = !this.isPanelOpen
            },
            navbarClick(element) {
                document.getElementById(element).scrollIntoView({behavior: "smooth", block: "center",});
                this.isPanelOpen = false
            }
        }
    }
</script>
<style>
    .slide-enter-active,
    .slide-leave-active
    {
        transition: transform 0.2s ease;
    }

    .slide-enter,
    .slide-leave-to {
        transform: translateX(-100%);
        transition: all 150ms ease-in 0s
    }

    .sidebar-backdrop {
        background-color: rgba(0,0,0,.5);
        width: 100vw;
        height: 100vh;
        position: fixed;
        top: 0;
        left: 0;
        cursor: pointer;
    }

    .sidebar-panel {
        overflow-y: auto;
        background-color: white;
        position: fixed;
        display: flex;
        flex-direction: column;
        left: 0;
        top: 0;
        height: 100vh;
        z-index: 999;
        padding: 3rem 20px 2rem 20px;
        width: 300px;
    }

    @media only screen and (max-width: 400px) {
        .sidebar-panel {
            width: 200px;
        }
    }
</style>