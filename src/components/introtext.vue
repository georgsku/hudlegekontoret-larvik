<template>
    <div class="wrapper margin-100" id="introtext">
        <div class="introtext">
            <h3>Om oss</h3>
            <p>Hudlegekontoret drives av hudlege Nad´a Rakovan. Hun er spesialist i hud- og veneriske sykdommer. <br>              
                Vi utreder og behandler alle slags hudsykdommer. 
                Praksisen har blant annet lysbehandling (smalspektret UVB - TL01) for helkropp, hender, 
                føtter og fotodynamisk behandling (PDT).
            </p>
            <p>
                Hudlegekontoret ligger i Sigurdsgate 4 – midt i byens gågate.
                Inngang nedenfor Apotek 1.
            </p>
            <div @click="mapClick">
                <img class="svg" src="../assets/location_icon.svg" width="25px" height="auto"/>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "introtext",
    methods: {
        mapClick() {
            document.getElementById("googlemaps").scrollIntoView({behavior: "smooth"});
        }
    }
}


</script>

<style scoped>
    .wrapper {
        display: flex;
        justify-content: center;
    }
    
    .introtext {
        width: 50vw;
    }

    .svg {
        cursor: pointer;
    }

    @media only screen and (max-width: 900px) {
        .introtext {
            width: 60vw;
            margin-bottom: 125px;
        }
    }

    @media only screen and (max-width: 700px) {
        .introtext {
            width: 70vw;
            margin-bottom: 100px;
        }
    }
    @media only screen and (max-width: 500px) {
        .introtext {
            width: 90vw;
            margin-bottom: 75px;
        }
    }

</style>