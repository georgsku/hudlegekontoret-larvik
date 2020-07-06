<template>
  <div class="header-container">
    <h1 id='headline'>Hudlegekontoret i Larvik</h1>
    <h2 id="subHeadline" v-html="'Dr. Na&#271;a Rakovan PhD'"></h2>
  </div>
</template>

<script>
export default {
  name: 'headerimage',
  
}
</script>

<style scoped>
  .header-container {
    background-image: url("https://images.pexels.com/photos/567973/pexels-photo-567973.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260");
    background-position: center center;
    height: 70vmin;
    min-height: 300px;
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    overflow: hidden;
  }

  #headline {
    text-shadow: 0px 0px 25px rgba(0,0,0,0.4); 
    margin: 40px 0 0 0;
  }
  
  #subHeadline {
    text-shadow: 0px 0px 25px rgba(0,0,0,0.4); 
    color: white; 
    margin: 15px 0;
  }


  @media only screen and (max-width: 825px) {
    #headline-image {
      width: auto;
      height: 100%;
    }
    
  }
</style>
