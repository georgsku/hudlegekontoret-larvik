<template>
    <div class="wrapper">
        <div class="introtext">
            <h3>Hudlegekontoret i Larvik</h3>
            <p>Praksisen drives av hudlege Nada Rakovan som er en kvinnelig spesialist i hud- og veneriske sykdommer. Vi utreder og behandler alle slags hudsykdommer. 
                Praksisen har bland annet lysbehandling (smalspektret UVB, - TL01) for helkropp, hender, føtter og fotodynamisk behandling (PDT).
            </p>
            <p>
                Hudlegekontoret ligger i Sigurdsgate 4 – midt i byens gågate.
                Inngang nedenfor Apotek 1.
            </p>
        </div>
    </div>
</template>

<script>
export default {
    name: "introtext"
}
</script>

<style scoped>
    .wrapper {
        display: flex;
        justify-content: center;
    }
    
    .introtext {
        width: 50vw;
        margin-bottom: 150px;
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