<script setup lang="ts">

import { onMounted, ref } from "vue";

type LeaderboardItem = { 
  player: string; 
  score: number; 
}
	
const leaderboardData = ref<LeaderboardItem[]>([]);
const errorMessage = ref(""); 
	
const url = 'http://localhost:3000/api/leaderboard-summary';

async function fetchLeaderboardData() {
  try {
    const response = await fetch(url)
    
    if (!response.ok) throw new Error(`Server Error ${response.status}`);
    
    leaderboardData.value = (await response.json()) as LeaderboardItem[];
  }
  catch (error: any) 
  {
    errorMessage.value = error?.message ?? "Unknown error";
  }
}

onMounted(() => {
  fetchLeaderboardData();
})

</script>

<template>
	<div class="leaderboard-summary">
    <h2>Leaderboard Summary</h2>
    <table>
      <thead>
      <tr>
        <th>Player</th>
        <th>Score</th>
      </tr>
      </thead>
      <tbody>
        <tr v-for="(item, index) in leaderboardData" :key="index">
          <td>{{ item.player }}</td>
          <td>{{ item.score }}</td>
        </tr>
      </tbody>
    </table>
    <p v-if="errorMessage" class="error{{ errorMessage }}"></p>
  </div>
</template>

<style scoped>

.leaderboard-summary {
  width: 500px;
  margin: 20px auto;
  padding: 15px;

  background: #fff;
  border: 1px solid #eee;
}

.leaderboard-summary h2 {
  margin-bottom: 10px;
  font-size: 16px;
  font-weight: 600;
  color: #222;
  text-align: center;
}

table
{
  width: 100%;
  border-collapse: collapse;
  font-size: 14px;
}

th, td {
  padding: 8px;
  border-bottom: 1px solid #e5e5e5;
  text-align: left;
}

th {
  background: #f6f6f6;
  font-weight: 600;
  color: #444;
}

.error 
{
  color: rebeccapurple;
}

</style>