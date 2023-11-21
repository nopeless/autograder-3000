<template>
  <div class="container mx-auto mt-8">
    <div class="flex flex-col space-y-4">
      <!-- Input for Rubric -->
      <input
        v-model="rubric"
        type="text"
        class="border p-2"
        placeholder="Enter Rubric"
      />

      <!-- Inputs for Student Answer and Solution -->
      <div class="flex space-x-4">
        <input
          v-model="studentAnswer"
          type="text"
          class="flex-1 border p-2"
          placeholder="Enter Student Answer"
        />
        <input
          v-model="solution"
          type="text"
          class="flex-1 border p-2"
          placeholder="Enter Solution"
        />
      </div>

      <!-- Submit Button -->
      <button
        class="bg-blue-500 text-white px-4 py-2 rounded-md"
        @click="submitForm"
      >
        Submit
      </button>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from "vue";

const rubric = ref("");
const studentAnswer = ref("");
const solution = ref("");

const submitForm = () => {
  // Handle form submission logic here
  console.log("Rubric:", rubric.value);
  console.log("Student Answer:", studentAnswer.value);
  console.log("Solution:", solution.value);
};
</script>
