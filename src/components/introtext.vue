<template>
    <div class="wrapper">
        <div class="introtext">
            <h3>Hudlegekontoret i Larvik</h3>
            <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. 
                Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, 
                when an unknown printer took a galley of type and scrambled it to make a type specimen book. 
                It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. 
                It was popularised in the 1960s with the release of Letraset sheets cont
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