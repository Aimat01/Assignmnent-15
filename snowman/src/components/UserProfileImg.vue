<template>
  <div class="containerProf">
    <div :class="`profile-image ${shape}`" :style="{ width: size, height: size }">
      <img src="./assets/WIN_20230501_18_40_38_Pro.jpg"/>
      <h4>Aimat and Arman</h4>
    </div>
  </div>
  </template>
  
  <script>
  export default {
    props: {
      altText: {
        type: String,
        default: 'Profile Image',
      },
      size: {
        type: String,
        default: '50px',
      },
      shape: {
        type: String,
        default: 'circle', // Can be 'circle' or 'square'
      },
    },
  };
  </script>
  
  <style>
  .containerProf{
    display: flex;
    justify-content: center;
  }
  .profile-image {
    display: flex;
    overflow: visible;
  }
  .profile-image img{
    width: 60px;
    height: 60px;
    border-radius: 50%;
  }
  .circle {
    border-radius: 50%;
  }
  
  .square {
    border-radius: 4px;
  }
  </style>
  