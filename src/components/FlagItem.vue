

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
      <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Dignissimos error reiciendis dicta. Consectetur
        sequi doloremque, dicta ea nemo dolore quisquam qui laborum dolorem quas rem neque. Aliquam ducimus magni
        dignissimos.
      </p>
    </div>
  </div>
</template>

<style scoped></style>

<script setup lang="ts">

interface FlagProps {
  id: number;
  title: string;
}

const flag = defineProps<FlagProps>()


</script>