<template>
    <div class="burger-menu-content">
      <router-link to="/">Home</router-link>
      <router-link to="/about">About Me</router-link>
      <router-link to="/hobby">Hobby</router-link>
      <router-link to="/contact">Contact</router-link>
    </div>
  </template>
  
  <script>
  export default {
    // Component logic here
  };
  </script>
  
  <style scoped>
  /* Burger menu content styles */
  .burger-menu-content {
    padding: 20px;
  }
  
  .burger-menu-content router-link {
    display: block;
    margin-bottom: 10px;
    color: black;
    text-decoration: none;
  }
  </style>
  