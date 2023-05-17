<template>
  <main class=" countrydetails px-3">

    <div class="w-full ">
      <img :src="countryInfo[0].flags.svg" :alt="countryInfo[0].name.common">
    </div>

    <div class="w-full countrydetails_content">
      <ul class="border-indigo-500">
        <li> Name: { countryInfo[0].name.common }}</li>
        <li>{{ countryInfo[0].capital }}</li>
        <li> {{ countryInfo[0].translations.ara.common }} </li>
        <li>altSpellings:
          <span v-for="item in countryInfo[0].altSpellings">
            {{ item }}
          </span>
        </li>
        <li></li>
        <li></li>
        <li></li>
        <li>googleMaps: <a :href="countryInfo[0].maps.googleMaps" target="_blank"> Go </a> </li>
      </ul>

    </div>

  </main>
</template>

<script setup lang="ts">

import { ref, onBeforeMount } from 'vue';
import axios from 'axios';
import { useRoute } from 'vue-router';

const route = useRoute();

const countryInfo = ref([]);

// console.log(route.params);

const countrydetails = () => {
  axios.get(`https://restcountries.com/v3.1/name/${route.params.name}`).then((response: any) => {
    console.log(response);
    countryInfo.value = response.data;
  });
  return countryInfo;
}

onBeforeMount(() => {
  return countrydetails();
})


</script>

<style scoped>
.countrydetails {
  background-color: #aaa;
  margin: 1rem 0;
  padding: 1rem 0;
  min-height: 500px;
  align-items: center;
}

.countrydetails img {
  width: 300px;
}

.countrydetails h1,
.countrydetails h2 {
  font-weight: bold;

}

.countrydetails_content {
  background-color: #eee;
  text-align: center;
}
</style>


