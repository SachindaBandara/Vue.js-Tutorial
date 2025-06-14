<script setup>
import { ref } from "vue";

const name = ref("Jhon Doe");
const status = ref("active");
const tasks = ref(["Task One", "Task Two", "Task Three"]);

const toggleStatus = () => {
  if (status.value === "active") {
    status.value = "pending";
  } else if (status.value === "pending") {
    status.value = "inactive";
  } else {
    status.value = "active";
  }
};
</script>

<template>
  <h1>{{ name }}</h1>

  <!-- if-else -->
  <!-- <p v-if="status">User is actve</p>
  <p v-else="status">User is inactve</p> -->

  <p v-if="status === 'active'">User is active</p>
  <p v-else-if="status === 'pending'">User is pending</p>
  <p v-else>User is inactive</p>

  <!-- for-each loop -->
  <h3>Tasks:</h3>
  <ul>
    <li v-for="task in tasks" :key="task">{{ task }}</li>
  </ul>

  <!-- bind two attributes -->
  <!-- <a v-bind:href="link">Click for Google</a> -->
  <!-- <a :href="link">Click for Google</a> -->
  <br />
  <br />
  <!-- toggle button -->
  <!-- <button v-on:click="toggleStatus">Change Status</button> -->
  <button @click="toggleStatus">Change Status</button>
</template>
