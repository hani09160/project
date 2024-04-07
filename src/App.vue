<template>
    <div id="app">
      <!-- Header -->
      <div class="header">
        <!-- Burger menu button -->
        <button class="burger-menu" @click="toggleMenu">
          <span></span>
          <span></span>
          <span></span>
        </button>
  
        <!-- Header links (visible only on larger screens) -->
        <div class="header-links" v-if="!isMenuOpen">
          <AppHeaderLinks />
        </div>
      </div>
  
      <!-- Burger menu content -->
      <div class="burger-menu-content" v-if="isMenuOpen">
        <!-- Header links (visible within the burger menu) -->
        <div class="burger-header-links">
          <AppHeaderLinks />
        </div>
      </div>
  
      <!-- Content -->
      <router-view />
  
      <!-- Footer -->
      <AppFooter />
    </div>
  </template>
  
  <script>
  import AppHeaderLinks from './components/shared/AppHeaderLinks.vue';
  import AppFooter from './components/shared/AppFooter.vue';
  
  export default {
    components: {
      AppHeaderLinks,
      AppFooter,
    },
    data() {
      return {
        isMenuOpen: false
      };
    },
    methods: {
      toggleMenu() {
        this.isMenuOpen = !this.isMenuOpen;
      }
    }
  };
  </script>
  
  <style scoped>
  /* General styles */
  body, #app {
    margin: 0;
    padding: 0;
  }
  
  /* Header styles */
  .header {
    background-color: #333;
    color: white;
    padding: 10px;
    text-align: center;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  
  /* Burger menu button styles */
  .burger-menu {
    background: transparent;
    border: none;
    cursor: pointer;
  }
  
  .burger-menu span {
    display: block;
    width: 30px;
    height: 3px;
    background-color: white;
    margin: 6px 0;
  }
  
  /* Header links styles */
  .header-links, .burger-header-links {
    display: flex;
  }
  
  .header-links a, .burger-header-links a {
    color: white;
    text-decoration: none;
    margin: 0 10px;
  }
  
  /* Burger menu content styles */
  .burger-menu-content {
    display: none;
  }
  
  /* Hide header links in mobile view */
  @media screen and (max-width: 768px) {
    .header-links {
      display: none;
    }
  
    .burger-menu-content {
      display: flex;
      flex-direction: column;
      align-items: center;
    }
  }
  </style>
  