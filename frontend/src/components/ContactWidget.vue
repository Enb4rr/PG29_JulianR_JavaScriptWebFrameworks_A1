<script setup lang="ts">
</script>

<template>
  <div class="contact-widget">
    <h2>Contact</h2>

    <input type="text" placeholder="First name" />
    <input type="text" placeholder="Last name" />
    <input type="email" placeholder="Email" />
    <input type="tel" placeholder="Phone number" />
    
    <button type="submit">Submit</button>
  </div>
</template>

<style scoped>
.contact-widget {
  width: 300px;
  margin: 20px auto;
  padding: 30px;

  background: #fff;
  border: 1px solid #eee;
}

.contact-widget h2 {
  margin-bottom: 10px;
  font-size: 16px;
  font-weight: 600;
  color: #222;
  text-align: center;
}

.contact-widget input {
  width: 100%;
  margin-bottom: 8px;
  padding: 6px 6px;

  font-size: 14px;
  border: 1px solid #ccc;
  outline: none;
}

.contact-widget button {
  padding: 10px 10px;
  margin: 5px 5px;
  border-radius: 6px;
  text-decoration: none;
  font-family: sans-serif;
  color: #444;
  background: #f6f6f6;
  border: 1px solid #e0e0e0;
  
  cursor: pointer;
}
</style>