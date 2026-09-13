<script setup lang="ts">
import IconHeadset from "@/components/icons/IconHeadset.vue";
</script>

<template>
  <header class="border-b flex justify-between shrink-0 font-bold">
    <div class="flex gap-4 items-center ml-10">
      <a href="#" class="text-gray-400">Settings</a>
      <a href="#" class="">Profile</a>
    </div>

    <div class="flex gap-4 p-5 items-center">
      <a href="#" class="border border-gray-300 rounded-lg text-sm p-2 flex items-center gap-2">
        <span class="text-gray-400">Tokens:</span>
        5/5
        <div class="w-20 h-1.5 bg-gray-400 rounded-full">
          <div class="h-full rounded-full bg-emerald-500" style="width: 100%">
          </div>
        </div>
      </a>
      <a href="#" class="border border-gray-300 rounded-lg p-2"> <IconHeadset/> </a>
    </div>
  </header>

</template>

<style scoped>

</style>