<script setup lang="ts">
const title = "Autograder 3000";
const description = "Automatically grades student answers based on a rubric.";
const features = [
  "Automated grading",
  "Customizable rubrics",
  "Instant feedback",
  "Detailed analytics",
];
</script>

<template>
  <div class="container">
    <h1>{{ title }}</h1>
    <p>{{ description }}</p>
    <ul>
      <li v-for="(feature, index) in features" :key="index">
        {{ feature }}
      </li>
    </ul>
    <nuxt-link to="/grader">Start Grading</nuxt-link>
  </div>
</template>

<style scoped>
.container {
  max-width: 800px;
  margin: 0 auto;
  padding: 2em;
  text-align: center;
}
</style>
