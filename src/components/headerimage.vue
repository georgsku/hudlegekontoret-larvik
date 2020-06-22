<template>
  <div class="header-container">
    <img id="headline-image" src="https://images.pexels.com/photos/167698/pexels-photo-167698.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260" />
    <h1 id='headline'>Hudlegekontoret I Larvik</h1>
  </div>
</template>

<script>
export default {
  name: 'headerimage',
  
}
</script>

<style scoped>
  .header-container {
    height: 70vh;
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-wrap: wrap;
    margin-bottom: 80px;
    position: relative;
    overflow: hidden;
    
  }

  #headline-image {
    filter:brightness(80%);
    background-position: center center;
  }

  #headline {
    position: absolute;
  }

  @media only screen and (max-width: 700px) {
    .header-image {
        height: 50vh;
      }
    
    #headline {
    }
  }

  @media only screen and (max-width: 500px) {
    
  }

</style>
