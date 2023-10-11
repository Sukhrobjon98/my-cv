<template>
  <div>
    <h1 class="text-[13px] md:text-[36px] md:font-bold my-5">LANGUAGE</h1>
    <hr class="h-1 bg-black rounded-[2px]" />
    <ul>
      <li
        v-for="(item, index) in data"
        :key="index"
        class="flex justify-between md:my-8"
      >
        <p class="md:text-2xl md:font-bold">{{ item?.language }}</p>
        <div class="grid grid-cols-5 gap-2 items-center">
          <div
            v-for="itemChild in item?.lavel"
            :key="item"
            :class="
              itemChild?.one
                ? `sx:w-3 sx:h-3 md:w-5 md:h-5 border-black border bg-black rounded-[50%]`
                : 'sx:w-3 sx:h-3 md:w-5 md:h-5 border-black border rounded-[50%]'
            "
          ></div>
        </div>
      </li>
    </ul>
  </div>
</template>
<script setup>
const data = [
  {
    language: "Uzbek",
    lavel: [
      {
        one: true,
      },
      {
        one: true,
      },
      {
        one: true,
      },
      {
        one: true,
      },
      {
        one: true,
      },
    ],
  },
  {
    language: "English",
    lavel: [
      {
        one: true,
      },
      {
        one: true,
      },
      {
        one: true,
      },
      {
        one: false,
      },
      {
        one: false,
      },
    ],
  },
];
</script>
<style scoped></style>
