<template>
    <div class="container">
    <div class="sidebar">
      <div class="sidebar-header">
        <h2>My Sidebar</h2>
      </div>
      <div class="sidebar-menu">
        <router-link to="/">Home</router-link>
        <router-link to="/about">About</router-link>
        <router-link to="/contact">Contact</router-link>
      </div>
    </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'Sidebar'
  };
  </script>
  
  <style scoped>
  .container{
    display: flex;
    justify-content: center;
    padding-top: 40px;
  }
  .sidebar {
    width: 250px;
    height: 100%;
    background-color: #333;
    color: #fff;
    padding-top: 20px;
  }
  
  .sidebar-header {
    text-align: center;
    padding-bottom: 20px;
  }
  
  .sidebar-menu {
    display: flex;
    justify-content: space-around;
  }
  
  .sidebar-menu router-link {
    color: #fff;
    text-decoration: none;
    padding: 10px;
    margin-bottom: 5px;
    transition: background-color 0.3s;
  }
  
  .sidebar-menu router-link:hover {
    color: #007bff;
  }
  </style>