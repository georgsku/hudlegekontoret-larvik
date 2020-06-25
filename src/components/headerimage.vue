<template>
  <div class="header-container">
    <img id="headline-image" src="https://images.pexels.com/photos/567973/pexels-photo-567973.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=750&w=1260" />
    <h1 id='headline'>Hudlegekontoret i Larvik</h1>
  </div>
</template>

<script>
export default {
  name: 'headerimage',
  
}
</script>

<style scoped>
  .header-container {
    height: 70vmin;
    min-height: 300px;
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
    margin-bottom: 80px;
    position: relative;
    overflow: hidden;
  }

  #headline-image {
    background-position: center;
  }

  #headline {
    position: absolute;
    text-shadow: 0px 0px 20px rgba(0,0,0,0.3);  
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
