<template>
    <div class="container">
        <div class="wrapper">
            <div class="wrapper-image">    
                <img class="image" src="../assets/article2.jpeg" alt="">
            </div>
            <div class="wrapper-text">    
                <h3>Åpningstid</h3>
                <p> vi har åpent fra:</p>
                <p> kl 09:00 - 1600 man - fre. <br> It is a long established fact that a reader will be distracted by the readable 
                    content of a page when looking at its layout
                </p>
            </div>
        </div>
        <div class="wrapper" style="margin: 200px 0 150px 0">
            <div class="wrapper-text">    
                <h3>Timebestillinger</h3>
                <p>It is a long established fact that a reader will be distracted by the readable 
                    content of a page when looking at its layout. The point of using Lorem Ipsum is 
                    that it has a more-or-less normal distribution of letters, as opposed to using 
                    'Content here, content here', making it look like readable English.
                </p>
            </div>
            <div class="wrapper-image">
                <img class="image" src="../assets/article2.jpeg" alt="">
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
        justify-content: center;
    }

    .wrapper-text {
        display: flex;
        align-items: center;
        flex-direction: column;
        justify-content: center;
        width: 30vw;
    }
    .wrapper-image {
        width: 30vw;
        margin: 0 40px;
    }

    .image {
        max-height: 100%;
        max-width: 100%;
        
    }
</style>