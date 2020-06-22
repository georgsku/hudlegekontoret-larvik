<template>
  <div class="header-image">
    <h1 id='headline'>Hudlegekontoret I Larvik</h1>
  </div>
</template>

<script>
export default {
  name: 'headerimage',
  
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .header-image {
   background-image: url('../assets/forest2.jpeg');
   background-position: center;
   filter: brightness(80%);
   height: 70vh;
   display: flex;
   align-items: center;
   justify-content: center;
   flex-wrap: wrap;
   margin-bottom: 80px;
   padding: 0 40px;
  }

  #headline {
    margin-top: 100px;
  }

  @media only screen and (max-width: 700px) {
    .header-image {
        height: 50vh;
      }
    
    #headline {
      margin-top: 50px;
    }
  }

  @media only screen and (max-width: 500px) {
    
  }

</style>
