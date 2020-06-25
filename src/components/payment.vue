<template>
    <div class="wrapper">
        <div class="introtext">
            <h3>Betaling</h3>
            <p>
                Egenandel er kr. 351,-<br>
                Barn under 16 år ingen egenandel.<br>
                Frikort gjelder.
            </p>
            <p>
                Materiell- og prøvekostander kommer i tillegg. <br>
                Gebyr for ikke benyttet time, gjelder også barn og personer med frikort.
            </p>
            <p>
                Vennligst unngå betaling med kontanter. Betaling med kort er ønskelig. <br>
                Vi har Bankterminal, men tar ikke kreditkort. <br>
                Girobetaling belastes med gebyr og administreres av Melin Medical.
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
        padding-top: 50px;
    }
    
    .introtext {
        width: 50vw;
        margin-bottom: 125px;
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