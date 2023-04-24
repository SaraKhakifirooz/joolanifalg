

<template>
  <main>

    <div class="flex w-full justify-center">
      <div v-for="(item, index) in flagdata" :key="index" class="w-[20%] mt-[1%] mr-[1%]">
        <FlagItem :id="index" :title="item.name" />
      </div>
    </div>

    <!-- <div class="flex flex-wrap w-full justify-center">
      <div v-for="(item, index) in flagscountryy" :key="index">
        <FlagCountry />
      </div>
    </div> -->

  </main>
</template>



<script setup lang="ts">

import { ref } from 'vue'
import FlagItem from '../components/FlagItem.vue'
import FlagCountry from '../components/FlagCountry.vue'

const flagdata = ref([
  { id: 0, name: 'IRAN' },
  { id: 1, name: 'USA' },
  { id: 2, name: 'ENGLAND' },
  { id: 3, name: 'CANADA' }
]);


// const flagscountryy = ref([
//   { id: 0, name: 'IRAN' },
//   { id: 1, name: 'USA' },
//   { id: 2, name: 'ENGLAND' },
//   { id: 3, name: 'CANADA' }
// ]);



</script>
