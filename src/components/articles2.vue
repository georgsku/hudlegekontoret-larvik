<template>
    <div class="container">
        <div class="wrapper" id="top-wrapper">
            <div class="wrapper-text">    
                <h3>Pasienter til lysbehandling</h3>
                <p> 
                    Alle lyspasienter må ha henvisning fra lege.
                </p>
                <p> 
                    Det koster kr. 56,- pr behandling inntil frikort er oppnåd<br>
                    Lyspasienter tas imot i kontorets åpningstider. <br>
                    Vi holder stengt for lysbehandling i lunsjen (kl 11:30 - 12:00) <br>
                    OBS: du må være her senest 15 min før stemgetid
                </p>
            </div>
            <div class="wrapper-image">
                <img class="image" src="../assets/lysbehandling.jpeg" alt="">
            </div>
        </div>
        <div class="border"/>
        <div class="wrapper" id="bot-wrapper">
            <div class="wrapper-image">    
                <img class="image" src="../assets/article6.jpeg" alt="">
            </div>
            <div class="wrapper-text">    
                <h3>Avbestilling av time</h3>
                <p>
                    Vær oppmerksom på at avbestilling må gjøres senest 24 timer før avtalt time 
                    på tlf 33 18 15 12 mellom kl 9:00 og 11:00 eller på mailadr post@rakovan.nhn.no 
                    før kl 15:00 to virkedager før timeavtalen
                </p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'articles'
}
</script>

<style scoped>
    .container {
        height: auto;
        width: 100%;
    }

    .wrapper {
        display: flex;
        flex-direction: row;
        justify-content: space-evenly;
    }

    #bot-wrapper {
        margin: 0 0 150px 0;
    }

    .wrapper-text {
        display: flex;
        align-items: center;
        flex-direction: column;
        justify-content: center;
        width: 40vw;
    }
    .wrapper-image {
        width: 32vw;
        margin: 0 40px;
        display: flex;
        align-items: center;
    }

    .image {
        max-height: 100%;
        max-width: 100%;
    }

    .border {
        border-bottom: 1.5px #f6b8b6 solid;
        border-radius: 2px;
        border-width: 70%;
        width: 70vw;
        margin: 100px auto;
    }

    @media only screen and (max-width: 700px) {
        .wrapper {
            flex-direction: column;
            align-items: center;
        }

        .wrapper-text {
            width: 70vw;
        }

        .wrapper-image {
            width: 70vw;
        }

        #bot-wrapper {
            margin: 100px 0 150px 0;
        }
     }

     @media only screen and (max-width: 700px) {

        #bot-wrapper {
            margin: 100px 0 100px 0;
        }
     }

     @media only screen and (max-width: 500px) {

        #bot-wrapper {
            margin: 100px 0 50px 0;
        }
     }
</style>