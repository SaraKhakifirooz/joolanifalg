<template>
  <div class="w-[300px] mt-[1%] mr-[1%]" >
    <div class="service-box">
      <div class="service-icon grey">
        <div class="front-content">
          <img :src="flagscountrydata.flags.svg" alt="{{ flagscountrydata.name.common }}">
          <i class="fa fa-trophy"></i>
          <h3>{{ flagscountrydata.name.common }}</h3>
        </div>
      </div>
      <div class="service-content">
        <h3>{{ flagscountrydata.name.common }}</h3>
        <p> {{ flagscountrydata.name.official }} </p>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref, onMounted } from 'vue'
import axios from 'axios'

interface Flagscountry {
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
    console.log(response);
    flagscountrydata.value = response.data
  });
}

onMounted(() => {
  flags();
})

</script>


<style scoped></style>
