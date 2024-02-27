<template>
  <div class="flex flex-col p-8">
    <div class="flex justify-center gap-2 mt-2">
      <router-link
        :to="{ name: 'byLetter', params: { letter } }"
        v-for="letter of letters"
        :key="letter"
      >
        {{ letter }}
      </router-link>
    </div>
  </div>
</template>

<script setup>
import { ref, onMounted } from "vue";
import store from "../store";
import axiosClient from "../axiosClient";

const letters = "ABCDEFGHIJKLMNOPQRSTUVWXYZ".split("");
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
