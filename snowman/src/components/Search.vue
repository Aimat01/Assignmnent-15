<template>
    <div class="container">
    <div class="search-bar">
      <input type="text" v-model="query" @input="search" placeholder="Search...">
      <button @click="search">Search</button>
    </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        query: ''
      }
    },
    methods: {
      search() {
        // Handle search logic here
        console.log(`Searching for: ${this.query}`);
      }
    }
  }
  </script>
  
  <style>
  .search-bar {
    display: flex;
    align-items: center;
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 4px;
  }
  
  .search-bar input {
    flex: 1;
    padding: 8px;
    margin-right: 10px;
    border: none;
    border-radius: 4px;
  }
  
  .search-bar button {
    padding: 8px 15px;
    border: none;
    border-radius: 4px;
    background-color: #007bff;
    color: #fff;
    cursor: pointer;
  }
  
  .search-bar button:hover {
    background-color: #0056b3;
  }
  </style>
  