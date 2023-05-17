

<template>
  <div class="service-box">
    <div class="service-icon yellow">
      <div class="front-content">
        <i class="fa fa-trophy"></i>
        <h3>{{ flag.title }}</h3>
      </div>
    </div>
    <div class="service-content">
      <h3>{{ flag.title }}</h3>
      <p>{{ flag.description }}</p>
    </div>
  </div>
</template>

<style scoped></style>

<script setup lang="ts">

import type { FlagProps } from '@/framework/Model';

const flag = defineProps<FlagProps>()

</script>