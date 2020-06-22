<template>
    <div class="container">
        <div class="wrapper" id="top-wrapper">
            <div class="wrapper-image">    
                <img class="image" src="../assets/article4.jpeg" alt="">
            </div>
            <div class="wrapper-text">    
                <h3>Åpningstid</h3>
                <p> vi har åpent fra:</p>
                <p> kl 09:00 - 1600 man - fre. <br> It is a long established fact that a reader will be distracted by the readable 
                    content of a page when looking at its layout
                </p>
            </div>
        </div>
        <div class="border"/>
        <div class="wrapper" id="bot-wrapper">
            <div class="wrapper-text">    
                <h3>Timebestillinger</h3>
                <p>It is a long established fact that a reader will be distracted by the readable 
                    content of a page when looking at its layout. The point of using Lorem Ipsum is 
                    that it has a more-or-less normal distribution of letters, as opposed to using 
                    'Content here, content here', making it look like readable English.
                </p>
            </div>
            <div class="wrapper-image">
                <img class="image" src="../assets/article5.jpeg" alt="">
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
        margin: 125px auto;
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