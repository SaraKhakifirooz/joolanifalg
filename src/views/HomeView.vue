<template>
  <main>
    <div class="flex w-full justify-center">
      <div v-for="(item, index) in flagdata" :key="index" class="w-[20%] mt-[1%] mr-[1%]">
        <FlagItem :code="item.id" :title="item.name" :description="item.content"/>
      </div>
    </div>
    <div class="flex flex-wrap w-full justify-center">
      <FlagCountries />
    </div>
  </main>
</template>

<script setup lang="ts">

import { ref } from 'vue'
import FlagItem from '../components/FlagItem.vue'
import FlagCountries from '../components/FlagCountries.vue';


const flagdata = ref([
  { id: 0, name: 'IRAN', content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit' },
  { id: 1, name: 'USA', content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit' },
  { id: 2, name: 'ENGLAND', content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit' },
  { id: 3, name: 'CANADA', content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit' }
]);

</script>
