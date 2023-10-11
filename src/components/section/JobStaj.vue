<template>
  <div>
    <h1 class="text-[13px] md:text-[36px] md:font-bold">
      PROFESSIONAL EXPERIENCE
    </h1>
    <hr class="h-1 bg-black rounded-[2px]" />
    <div v-for="item in Jobdata" :key="item?.id">
      <h1 class="font-bold md:text-[25px]">{{ item?.job }}</h1>
      <div class="grid grid-cols-2">
        <div class="flex items-end">
          <img :src="building" alt="icon" class="w-[20%] max-w-[40px]" />
          <span class="sx:text-[13px] sm:text-[13px] lg:text-[20px]">{{
            item?.place
          }}</span>
        </div>
        <div class="grid grid-cols-2">
          <div class="flex items-center gap-1">
            <img :src="date" alt="icon" class="sx:w-[22%] max-w-[25px]" />
            <p
              class="sx:text-[8px] sm:text-[12px] xl:text-[16px] flex justify-end"
            >
              {{ item?.date }}
            </p>
          </div>
          <div class="flex items-center gap-1">
            <img :src="located" alt="icon" class="w-[20%] max-w-[18px]" />
            <p
              class="sx:text-[9px] sm:text-[12px] xl:text-[16px] flex justify-end"
            >
              {{ item?.laktation }}
            </p>
          </div>
        </div>
        <div class="md:gap-1 flex items-center">
          <img
            :src="link"
            alt="icon"
            class="sx:w-[22%] max-w-[25px] rotate-[-45deg]"
          />
          <a :href="item?.link" class="font-bold md:text-[16px]"
            >{{ item?.linkName }}|</a
          >
          <span class="sx:text-[10px] md:text-[15px]">{{
            item?.linkNameAfter
          }}</span>
        </div>
      </div>
      <ul class="list-disc mt-2">
        <li v-for="itemChild in item?.texts" class="md:text-[1.5rem] py-1 ">
          {{ itemChild?.dataText }}
        </li>
      </ul>
    </div>
  </div>
</template>
<script setup>
import building from "../../assets/svg/building.svg";
import located from "../../assets/svg/located.svg";
import date from "../../assets/svg/date.svg";
import link from "../../assets/svg/link.svg";
import {Jobdata}  from '../../const/const-datas.js'
</script>
<style scoped></style>
