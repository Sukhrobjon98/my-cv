<template>
  <div>
    <h1 class="text-[13px] md:text-[36px] md:font-bold">SOFT SKILLS</h1>
    <hr class="h-1 bg-black rounded-[2px]" />
    <div class="flex flex-wrap gap-2 mt-8">
      <span
        v-for="(item, index) in softSkills"
        :key="index"
        class="p-2 border sx:text-[13px] md:text-2xl font-bold"
        >{{ item?.name }}</span
      >
    </div>
  </div>
</template>
<script setup>
import { softSkills } from '../../const/const-datas';
</script>
<style scoped></style>
