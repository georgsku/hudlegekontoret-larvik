<template>
    <div class="container">
        <div class="border"/>
        <div class="wrapper" id="timebestillinger">
            <div class="wrapper-text">    
                <h3>Timebestillinger</h3>
                <p> 
                    Kontoret har driftsavtale med Helse Sør-Øst RHF og det kreves derfor henvisning fra lege for å få time hos oss.<br>
                    Alle tidligere pasienter med nye problemstillinger må også ha henvisning fra lege.<br>
                    Henvisninger vurderes av hudlege før timeavtale settes opp.
                    Sørg for at riktig postadresse og mobiltelefonnummer er påført henvisning. 
                    Det er henvisende lege sitt ansvar å beskrive ditt problem, slik at det er mulig å prioritere din henvisning riktig. </p>
                <p> 
                    <strong>Det er stor pågang av henvisninger.</strong> <br>
                    Ventetiden varierer og kan være opptil 8 mnd. 
                </p>
                <p> 
                    Enkelte diagnoser prioriteres høyt. <br>
                    Rene kosmetiske problemstillinger prioriteres ikke.
                    Vi har ikke laserbehandling.
                </p>
                <p> 
                    <strong>Forverring av problem i påvente av timen:
                    Ta kontakt med henvisende lege.</strong>
                </p>
            </div>
            <div class="wrapper-image">
                <img class="image" src="../assets/undersøkelse.jpeg" alt="">
            </div>
        </div>
        <div class="border"/>
        <div class="wrapper" id="åpningstimer">
            <div class="wrapper-text">    
                <h3>Åpningstider</h3>
                <p>Mandag 8:00 - 16:30 <br> 
                Tirsdag 8:00 - 16:00 <br> 
                Onsdag 8:00 - 16:30 <br> 
                Torsdag 8:00 - 16:00 <br> 
                Fredag 8:00 - 14:00 <br> 
                </p>
                <p>Hudlegen er ikke tilstede i klinikkens hele åpningstid.</p>
                <p>Vi har stengt i forbindelse med jul og påske, og alle røde dager.</p>
            </div>
            <div class="wrapper-text">    
                <h3>Telefontid</h3>
                <p>
                    Mandag - Fredag<br> 9:00 - 11:00
                </p>
                <p>
                    Vi har stor pågang av pasienter og det kan være vanskelig å komme gjennom på telefon<br> 
                </p>
                <p>
                    Vårt tlf nr er: 33 18 15 12.
                </p>
            </div>
        </div>
        <div class="border"/>
        <div class="wrapper" id="lysbehandling">
            <div class="wrapper-text">    
                <h3>Lysbehandling</h3>
                <p> 
                    Alle pasienter som skal ha lysbehandling må ha henvisning fra lege.
                </p>
                <p> 
                    Det koster kr. 58,- pr behandling inntil frikort er oppnåd.<br>
                    Pasienter til lysbehandling tas imot i kontorets åpningstid. <br>
                    Vi holder stengt for lysbehandling i lunsjen (kl 11:30 - 12:00). <br>
                    <strong>OBS:</strong> oppmøte senest 15 min før stengetid
                </p>
            </div>
            <div class="wrapper-image">
                <img class="image" src="../assets/lysbehandling.jpeg" alt="">
            </div>
        </div>
        <div class="border"/>
        <div class="wrapper" id="avbestilling" >
            <div class="wrapper-image">    
                <img class="image" src="../assets/article6.jpeg" alt="">
            </div>
            <div class="wrapper-text">    
                <h3>Avbestilling av time</h3>
                <p>
                    Vær oppmerksom på at avbestilling må gjøres senest 24 timer før avtalt time 
                    på tlf 33 18 15 12 mellom kl 9:00 og 11:00 eller på mail; post@rakovan.nhn.no 
                    før kl 15:00 to virkedager før timeavtalen
                </p>
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
        margin: 0 auto;
        width: 80%;
        display: flex;
        flex-direction: row;
        padding: 50px 0;
    }

    .wrapper-text {
        margin: auto;
        width: clamp(45ch, 50%, 65ch);
    }
    .wrapper-image {
        width: 32vw;
        margin: 0 40px;
        display: flex;
        align-items: center;
        justify-content: center;
    }

    .image {
        height: auto;
        width: 100%;
        max-width: 500px;
        border-radius: 10px;
        -webkit-box-shadow:4px 4px 0px 1px rgba(0,0,0,0.20); 
        box-shadow: 4px 4px 0px 1px rgba(0,0,0,0.20);;
    }

    .border {
        border-bottom: 1.5px #f6b8b6 solid;
        border-radius: 2px;
        border-width: 70%;
        width: 70vw;
        margin: 100px auto;
    }

    @media only screen and (max-width: 800px) {
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

        .border {
        margin: 80px auto;
    }
     }

     @media only screen and (max-width: 500px) {

        .border {
            margin: 60px auto;
        }
     }
</style>