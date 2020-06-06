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
   height: 70vh;
   display: flex;
   align-items: center;
   justify-content: center;
   margin-bottom: 80px;
  }

  #headline {
    margin-top: 100px;
  }
</style>
