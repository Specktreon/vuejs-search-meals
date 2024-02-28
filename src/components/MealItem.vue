<template>
  <div class="bg-white shadow rounded-xl">
    <router-link :to="{ name: 'mealDetails', params: { id: meal.idMeal } }">
      <img
        :src="meal.strMealThumb"
        :alt="meal.strMeal"
        class="rounded-t-xl w-full h-64 object-cover"
      />
    </router-link>
    <div class="p-3">
      <h3 class="font-semibold">{{ meal.strMeal }}</h3>
      <p class="mb-5">
        this is the meal you donwloaded from firgirl repack twodays ago when i
        was raining in the summer
      </p>
      <div class="flex items-center justify-between">
        <youtube-button :href="meal.strYoutube"> Youtube </youtube-button>
      </div>
    </div>
  </div>
</template>

<script setup>
import YoutubeButton from "../components/YoutubeButton.vue";

const { meal } = defineProps({
  meal: {
    required: true,
    type: Object,
  },
});
</script>
