<template>
     <div class="footer">
        <iframe
            title="googlemaps"
            id="googlemaps"
            class="google-map"
            width="500"
            height="350"
            frameborder="0"
            src="https://www.google.com/maps/embed/v1/place?key=AIzaSyDRv9pdj_xklj8b54g7WMAaQ7OxM6NSaU4
                &q=hudlegekontoret+i+larvik" allowfullscreen>
        </iframe>
        <div class="footer-text">
            <h3><span style="font-weight: 100;">Na&#271;a</span><span style="font-weight: 600;">Rakovan</span></h3>
            <p>Tlf: 33 18 15 12</p>
            <p>Sigurds gate 4, 3256 Larvik</p>
        </div>
    </div>
</template>

<script>
export default {
    name: "footer"
}

</script>

<style scoped>
.footer {
    width: 100%;
    padding: 30px 0;
    background-color: #f6b8b6;
    color: #F7F8EB;
    text-align: center;
    position: relative;
    display: flex;
    flex-direction: row;
    justify-content: space-evenly;
    align-items: center;
  }

  .google-map {
    max-width: 90%;
    border: #534859 3px solid ;
    border-radius: 10px;
    --tw-shadow: 0 1px 3px 0 rgba(0, 0, 0, 0.1), 0 1px 2px 0 rgba(0, 0, 0, 0.06);
    box-shadow: var(--tw-ring-offset-shadow, 0 0 #0000), var(--tw-ring-shadow, 0 0 #0000), var(--tw-shadow);
  }

  @media only screen and (max-width: 700px) {
        .footer {
            flex-direction: column;
        }
    }

</style>