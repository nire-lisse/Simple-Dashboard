<script setup lang="ts">
import IconHeadset from "@/assets/icons/Headset.svg";
</script>

<template>
  <header class="border-b flex justify-between shrink-0 font-medium border-[#E9EBEF] px-9 py-3 bg-white h-16">
    <div class="flex gap-2.5 items-center text-sm">
      <a href="#" class="text-[#9399AF]">Settings</a>
      <a href="#" class="text-[#3F455E]">Profile</a>
    </div>

    <div class="flex gap-2 items-center text-xs">
      <a href="#" class="border border-[#E9EBEF] rounded-lg px-3 py-4 flex items-center gap-3 h-10">

        <div class="gap-2 flex">
          <div class="text-[#9399AF]">Tokens:</div>
          <div class="text-[#3F455E]">5/5</div>
        </div>

        <div class="w-20 h-1.5 bg-gray-400 rounded-[100px]">
          <div class="h-full rounded-[100px] bg-[#00B194]" style="width: 100%">
          </div>
        </div>
      </a>
      <a href="#" class="border border-[#E9EBEF] bg-[#F9FBFC] rounded-lg size-10 flex items-center justify-center">
        <IconHeadset/>
      </a>
    </div>
  </header>
</template>

<style scoped>

</style>