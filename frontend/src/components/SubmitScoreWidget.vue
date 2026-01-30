<script setup lang="ts">

</script>

<template>
<div class="submit-score-widget">
  <h1>Submit new score</h1>
  
  <div class="submit-score-container">
    <input type="text" placeholder="Score" />
    <button class="submit-button">Submit</button>
  </div>
  
</div>
</template>

<style scoped>

.submit-score-widget {
  width: 500px;
  margin: 20px auto;
  padding: 15px;

  background: #fff;
  border: 1px solid #eee;
}

.submit-score-widget h1 {
  font-size: 15px;
  font-weight: normal;
}

.submit-score-container {
  display: flex;
}

.submit-score-container button {
  padding: 10px;
  margin: 5px;
  border-radius: 6px;
  text-decoration: none;
  font-family: sans-serif;
  color: #444;
  background: #f6f6f6;
  border: 1px solid #e0e0e0;
  cursor: pointer;
}

.submit-score-container input {
  width: 100%;
  margin: 5px;
  padding: 6px;

  font-size: 14px;
  border: 1px solid #ccc;
  outline: none;
}

</style>