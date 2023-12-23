<template>
    <div :class="['drawer', { 'open': isOpen }]">
      <div class="drawer-content">
        <slot></slot>
      </div>
      <div class="drawer-handle" @click="toggleDrawer">
        Open Drawer
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        isOpen: false,
      };
    },
    methods: {
      toggleDrawer() {
        this.isOpen = !this.isOpen;
      },
    },
  };
  </script>
  
  <style>
  .drawer {
    /* styling for the drawer component */
    width: 300px;
    height: 100%;
    background-color: #fff;
    position: fixed;
    top: 0;
    right: -300px;
    transition: right 0.3s ease-in-out;
  }
  .drawer.open {
    right: 0;
  }
  .drawer-handle {
    /* styling for the handle to open the drawer */
    cursor: pointer;
    position: fixed;
    top: 50%;
    right: 10px;
    background-color: #ccc;
    padding: 10px;
    border-radius: 5px;
  }
  </style>
  