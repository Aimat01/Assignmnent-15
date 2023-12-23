<template>
    <div class="containerHead">
        <div class="page-header">
            <h1>{{ title }}</h1>
            <p v-if="description">{{ description }}</p>
        </div>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      title: {
        type: String,
        required: true
      },
      description: {
        type: String,
        default: ''
      }
    }
  }
  </script>
  
  <style>
  .containerHead{
    padding-top: 40px;
  }
  .page-header {
    padding: 20px;
    color: black;
    background-color: #f5f5f5;
    border-bottom: 1px solid #ddd;
  }
  
  .page-header h1 {
    margin: 0;
    font-size: 24px;
  }
  
  .page-header p {
    margin-top: 10px;
    font-size: 16px;
    color: #777;
  }
  </style>
  