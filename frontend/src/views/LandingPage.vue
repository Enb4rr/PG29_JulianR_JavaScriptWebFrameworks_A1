<script setup lang="ts">
  import LeaderboardSummaryWidget from "@/components/LeaderboardSummaryWidget.vue";
  import SubmitScore from "@/components/SubmitScoreWidget.vue";
  import DescriptionWidget from "@/components/DescriptionWidget.vue";
</script>

<template>
  <div class="landing-page">
    <DescriptionWidget />
    <LeaderboardSummaryWidget />
    <SubmitScore />
  </div>
</template>

<style scoped>
  .landing-page {
    font-family: sans-serif;
    text-align: center;
    margin-top: 10px;
  }
</style>