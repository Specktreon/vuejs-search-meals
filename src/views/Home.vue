<template>
  <div class="flex flex-col p-8"></div>
</template>

<script setup>
import { ref, onMounted } from "vue";
import store from "../store";
import axiosClient from "../axiosClient";

const ingredients = ref([]);

onMounted(async () => {
  try {
    const response = await axiosClient.get("list.php?i=list");
    ingredients.value = response.data;
    console.log(response.data);
  } catch (error) {
    console.error("Error fetching data:", error);
  }
});
</script>
