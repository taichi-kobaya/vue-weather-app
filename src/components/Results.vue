<template>
  <div class="results-country" v-if="results.country">{{ country }}</div>
  <div class="results-city" v-if="results.cityName">{{ cityName }}</div>
  <div class="results-temp" v-if="results.temperature">{{ temperature }}</div>
  <div class="results-condition" v-if="results.icon">
    <img :src="icon" alt="icon">
    <span>{{ conditionText }}</span>
  </div>
</template>

<script setup>
  import { toRefs } from "vue"

  const props = defineProps({
    results: Object
  })

  const { country, cityName, temperature, icon, conditionText } = toRefs(props.results)
</script>