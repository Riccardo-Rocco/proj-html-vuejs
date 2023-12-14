<template>
  <!--components post shipping e discount 70%-->
    <div class="background-component">
      <div class="content-container">
        <div class="image-with-text">
          <img src="../assets/images/promo_box_1_bg.jpg" alt="Background Image">
          <div class="text-overlay">
            <h2>70% Off</h2>
            <p>Vivamus tempor leo lacus, feugiat, ut magna aliquam erat.</p>
            <button @click="handleButtonClick">VIEW MORE</button>
          </div>
        </div>
        <div class="image-with-text">
          <img src="../assets/images/promo_box_2_bg.jpg" alt="Second Image">
          <div class="text-overlay">
            <h2>Free Shipping</h2>
            <p>Vivamus tempor leo lacus, feugiat ut magna aliquam erat.</p>
            <button @click="handleButtonClick">VIEW MORE</button>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    methods: {
      handleButtonClick() {
        console.log('Hai cliccato sul bottone');
      },
    },
  };
  </script>
  
  <style scoped>
  .background-component {
    background: url('../assets/images/bkgd_confetti-compressor.jpg') center/cover no-repeat;
    padding: 50px;
    
  }
  
  .content-container {
    display: flex;
    justify-content: space-evenly;
    
    
  }
  
  .image-with-text {
    position: relative;
    width: 43%;
  }
  
  .text-overlay {
    position: absolute;
    top: 50%;
    left: 35%;
    transform: translate(-50%, -50%);
    padding: 20px;
    color: #fff;
    text-align: left;
    
  }
  
  .text-overlay h2 {
    font-size: 2em;
    margin-bottom: 10px;
  }
  
  .text-overlay p {
    font-size: 1.2em;
    margin: 0;
  }
  
  .text-overlay button {
    padding: 10px 20px;
    font-size: 1em;
    background-color: transparent;
    color: #fff;
    border: solid 1px white;
    border-radius: 20px;
    cursor: pointer;
    margin-top: 0.5rem;

  }
  
  
  .image-with-text img {
    max-width: 100%;
    height: auto;
   
  }
  </style>
  