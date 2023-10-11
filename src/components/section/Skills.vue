<template>
  <div>
    <h1 class="text-[13px] md:text-[36px] md:font-bold ">TECH SKILLS</h1>
    <hr class="h-1 bg-black rounded-[2px]" />
    <div class="flex flex-wrap gap-2 mt-5">
      <span
        v-for="(item, index) in techSkills"
        :key="index"
        class="p-2 border sx:text-[13px] md:text-2xl px-4 py-3  mx-1 my-1 font-bold"
        >{{ item?.name }}</span
      >
    </div>
  </div>
</template>
<script setup>
import{techSkills} from "../../const/const-datas.js"
</script>
<style scoped></style>
