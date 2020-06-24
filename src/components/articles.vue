<template>
    <div class="container">
        <div class="wrapper" id="top-wrapper">
            <div class="wrapper-text">    
                <h3>Timebestillinger</h3>
                <p> 
                    Kontoret har driftsavtale med Helse Sør-Øst RHF og krever derfor henvisning fra lege for å få time hos oss.<br>
                    Alle tidligere pasienter med nye problemstillinger må også ha henvisning fra lege.<br>
                    Henvisninger vurderes av hudlege før timeavtale settes opp.
                    Sørg for at riktig postadresse og mobiltelefonnummer er påført henvisning. 
                    Det er henvisende lege sitt ansvar å beskrive ditt problem, slik at det er mulig å prioritere din henvisning riktig. </p>
                <p> 
                    <strong>Det er stor pågang av henvisninger.</strong> <br>
                    Ventetiden varierer og kan være opptil 8 mnd. 
                </p>
                <p> 
                    Diagnoser som f.eks. føflekkreft prioriteres høyt. <br>
                    Rene kosmetiske problemstillinger prioriteres ikke.
                    Vi har ikke laserbehandling.
                </p>
                <p> 
                    <strong>Forverring av problem i påvente av timen:
                    Ta kontakt med din fastlege.</strong>
                </p>
            </div>
            <div class="wrapper-image">
                <img class="image" src="../assets/undersøkelse.jpeg" alt="">
            </div>
        </div>
        <div class="border"/>
        <div class="wrapper" id="bot-wrapper">
            <div class="wrapper-image">    
                <img class="image" src="../assets/article4.jpeg" alt="">
            </div>
            <div class="wrapper-text">    
                <h3>Åpningstider</h3>
                <p>Mandag 8:00 - 16:30 <br> 
                Tirsdag 8:00 - 16:00 <br> 
                Onsdag 8:00 - 16:30 <br> 
                Torsdag 8:00 - 16:00 <br> 
                Fredag 8:00 - 14:00 <br> 
                </p>
                <p>Hudlegen er ikke tilstede i hele klinikkens åpningstider.</p>
                <p>Vi har stengt i forbindelse med jul og påske, og alle røde dager.</p>
            </div>
        </div>
        <div class="border"/>
        <div class="wrapper" id="bot-wrapper">
            <div class="wrapper-text">    
                <h3>Telefontid</h3>
                <p>
                    Mandag - Fredag: 9:00 - 11:00
                </p>
                <p>
                    Vi har stor pågang av pasienter og det kan være vanskelig å omme gjennom på telefon<br> 
                </p>
                <p>
                    Vårt tif nr er: 33 19 15 12.
                </p>
            </div>
            <div class="wrapper-image">    
                <img class="image" src="../assets/article4.jpeg" alt="">
            </div>
        </div>
        <div class="border"/>
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