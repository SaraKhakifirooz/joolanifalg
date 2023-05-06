<template>
  <!-- Flag countries -->
  <div v-for="(item, index) in flagscountrydata" :key="index">
    <FlagCountry :id="index" :svg="item.flags.svg" :commonName="item.name.common" :OfficialName="item.name.official" />
  </div>
</template>

<script setup lang="ts">
import { ref, onMounted } from 'vue';
import axios from 'axios';
import FlagCountry from './FlagCountry.vue';

interface Flagscountry {
  id: number;
  flags: Image;
  name: Name;
}

interface Name {
  common: string;
  official: string;
}

interface Image {
  png: string;
  svg: string;
  alt: string;
}

const flagscountrydata = ref<Flagscountry[]>([]);

const flags = async () => {
  return await axios.get('https://restcountries.com/v3.1/all?fields=name,flags').then((response) => {
    flagscountrydata.value = response.data
  });
}

onMounted(() => {
  flags();
})

</script>


<style scoped></style>
