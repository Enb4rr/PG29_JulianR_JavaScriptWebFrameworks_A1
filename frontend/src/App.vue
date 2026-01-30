<script setup lang="ts">
  const year = new Date().getFullYear()
</script>

<template>
  <div id="app">
    <header class="header">
      
      <div class="title">
        Julian's cool game
      </div>
      
      <nav>
        <router-link class="router-button" to="/">Home</router-link>
        <router-link class="router-button" to="/contact">Contact</router-link>
      </nav>
    </header>
    <main>
      <router-view></router-view>
    </main>
    <footer class="footer">
      <p>© {{ year }} Julian's cool game. All rights reserved.</p>
    </footer>
  </div>
</template>

<style scoped>

  #app {
    min-height: 90vh;
    display: flex;
    flex-direction: column;
  }
  
  main {
    display: flex;
    flex-direction: column;
    justify-content: center;
  }

  .header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 20px;
    background: white;
    border-bottom: 1px solid #eee;
  }

  .title {
    font-size: 40px;
    color: #222;
  } 

  .router-button {
    padding: 10px 10px;
    margin: 5px 5px;
    border-radius: 6px;
    text-decoration: none;
    font-family: sans-serif;
    color: #444;
    background: #f6f6f6;
    border: 1px solid #e0e0e0;
  }

  .footer {
    padding: 20px;
    background: #fafafa;
    border-top: 1px solid #eee;
    text-align: center;
    color: #777;
    
    width: 100%;
    
    position: fixed;
    bottom: 0px;
  }
  
</style>
