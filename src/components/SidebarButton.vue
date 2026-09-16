<script setup lang="ts">
import {computed} from "vue";

const {active, textColor} = defineProps<{
  active?: boolean
  textColor?: string
}>()

const classes = computed(() => {
  let tempClass = []

  if (active) {
    if (!textColor)
      tempClass.push('text-white')

    tempClass.push('bg-[#393E5C]')
  } else {
    if (!textColor)
      tempClass.push('text-[#9399AF]')
  }

  return tempClass.join(' ')
})
</script>

<template>
  <a href="#"
     class="flex items-center gap-3 p-3 rounded-lg hover:bg-slate-600 transition-colors"
     :class="classes"
     :style="textColor ? { color: textColor } : undefined">
    <slot name="icon"/>
    <slot name="text"/>
  </a>
</template>

<style scoped>

</style>