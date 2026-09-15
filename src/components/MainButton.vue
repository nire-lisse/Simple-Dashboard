<script setup lang="ts">

</script>

<template>
  <div class="flex items-center p-5 border border-[#E9EBEF] rounded-lg gap-5 w-full">
    <div class="size-10 bg-[#E6FAF7] rounded-sm flex items-center justify-center text-[#00B194]">
      <slot name="icon"/>
    </div>

    <div class="gap-1">
      <div class="font-semibold text-[#3F455E]">
        <slot name="h1"/>
      </div>
      <div class="text-[#9399AF]">
        <slot name="h2"/>
      </div>
    </div>
  </div>
</template>

<style scoped>

</style>