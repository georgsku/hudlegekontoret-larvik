<template>
    <div class="wrapper margin-100" id="betaling">
        <div class="introtext">
            <h3>Betaling</h3>
            <p>
                Egenandel er kr. 386,-<br>
                Barn under 16 år betaler ingen egenandel.<br>
                Frikort gjelder.
            </p>
            <p>
                Materiell- og prøvekostnader kommer i tillegg. <br>
                Gebyr for ikke benyttet time gjelder også barn og personer med frikort.
            </p>
            <p>
                Vennligst unngå betaling med kontanter. Betaling med kort er ønskelig. <br>
                Vi har bankterminal, men tar ikke kredittkort. <br>
                Girobetaling belastes med gebyr og administreres av Convene Collection.
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