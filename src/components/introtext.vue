<template>
    <div class="wrapper margin-100" id="introtext">
        <div class="introtext">
            <h3>Julen 2020</h3>
            <p>
                Hudlegekontoret er stengt f.o.m 21.12.20.
            </p>
            <p>
                Vi åpner igjen mandag 4.1.21.
            </p>
            <p>
                Vi ønsker alle en riktig god jul!
            </p>
            <h3 class="seperate-header">Om oss</h3>
            <p>Hudlegekontoret drives av hudlege Na&#271;a Rakovan. Hun er spesialist i hud- og veneriske sykdommer. <br>              
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
    .seperate-header {
        padding-top: 50px;
    }

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
        }
    }

    @media only screen and (max-width: 700px) {
        .introtext {
            width: 70vw;
        }
    }
    @media only screen and (max-width: 500px) {
        .introtext {
            width: 90vw;
        }
    }

</style>