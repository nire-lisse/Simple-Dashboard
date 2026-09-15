<script setup lang="ts">

import IconArrowRight from "@/assets/icons/ArrowRight.svg";
import {computed} from "vue";

type statusType = 'Done' | 'In progress' | 'Declined'

const {status} = defineProps<{
  status?: statusType;
}>()

const Status = computed(() => {
  switch (status) {
    case 'Done':
      return {label: "Done", class: "bg-[#E6FAF7] text-[#00B194]"};
    case 'In progress':
      return {label: "In progress", class: "bg-[#FFF9E6] text-[#E79900]"};
    case 'Declined':
      return {label: "Declined", class: "bg-[#FFECEC] text-[#FF4A4A]"};
    default:
      return {label: "Error", class: "bg-red-900 text-red-300"}
  }
})
</script>

<template>
  <tr class="text-xs">
    <td class="text-left px-6 gap-1 flex flex-col justify-center h-12">
      <div class="text-[#272C43]">Arsenal vs Chelsea</div>
      <div class="text-[#9399AF]">English Premier League - 12.02.2026</div>
    </td>
    <td class="text-[#272C43]">John Doe</td>
    <td class="text-[#272C43]">April 15</td>
    <td><span class="rounded-full px-2 py-1" :class="Status.class">{{Status.label}}</span></td>
    <td class="text-[#9399AF]">
      <slot name="Data"/>
    </td>
    <td>
      <a href="#" class="flex gap-4 items-center">
        View
        <IconArrowRight/>
      </a>
    </td>
  </tr>
</template>

<style scoped>

</style>