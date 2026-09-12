<script setup lang="ts">
import IconChevronLeft from "@/components/icons/IconChevronLeft.vue";
import IconPlus from "@/components/icons/IconPlus.vue";
import IconHome from "@/components/icons/IconHome.vue";
import IconTrophy from "@/components/icons/IconTrophy.vue";
import IconLayout from "@/components/icons/IconLayout.vue";
import IconSettings from "@/components/icons/IconSettings.vue";
import IconAskAI from "@/components/icons/IconAskAI.vue";
import IconLogOut from "@/components/icons/IconLogOut.vue";
import IconChevronRight from "@/components/icons/IconChevronRight.vue";
import TheWelcome from './components/TheWelcome.vue'

import {ref} from "vue";

const isSidebarOpen = ref(true);

function toggleSidebar() {
  isSidebarOpen.value = !isSidebarOpen.value;
}
</script>

<template>
  <aside class="bg-gray-900 shrink-0 flex flex-col transition-all duration-300 overflow-hidden"
         :class="isSidebarOpen ? 'w-64' : 'w-20'">
    <header class="text-white text-xl p-5 flex justify-between items-center italic font-mono  font-extrabold">
      <h2 class="pl-5" v-if="isSidebarOpen">
        STATS
      </h2>

      <button
          class="flex items-center justify-center w-9 h-9 bg-slate-800 rounded-lg cursor-pointer hover:bg-slate-700 transition-colors"
          @click="toggleSidebar">
        <IconChevronLeft v-if="isSidebarOpen"/>
        <IconChevronRight v-else/>
      </button>
    </header>

    <hr class="mx-6 border-gray-800" v-if="isSidebarOpen"/>

    <nav class="justify-center  flex m-6 text-sm font-semibold font-mono h-full" v-if="isSidebarOpen">
      <ul class="space-y-5 w-full">
        <li class="text-white p-3 rounded-lg bg-teal-500 hover:bg-teal-400 transition-colors">
          <a href="#" class="flex gap-3">
            <IconPlus/>
            Create order
          </a>
        </li>
        <li class="text-white p-3 rounded-lg bg-slate-700 hover:bg-slate-600 transition-colors">
          <a href="#" class="flex gap-3">
            <IconHome/>
            Dashboard
          </a>
        </li>
        <li class="text-amber-400 p-3 rounded-lg hover:bg-slate-800 transition-colors">
          <a href="#" class="flex gap-3">
            <IconTrophy/>
            World Cup 2026
          </a>
        </li>
        <li class="text-gray-500 p-3 rounded-lg hover:bg-slate-800 transition-colors">
          <a href="#" class="flex gap-3">
            <IconLayout/>
            Free datasets
          </a>
        </li>
        <li class="text-gray-500 p-3 rounded-lg hover:bg-slate-800 transition-colors">
          <a href="#" class="flex gap-3">
            <IconSettings/>
            Settings
          </a>
        </li>
        <li class="text-gray-500 p-3 rounded-lg hover:bg-slate-800 transition-colors">
          <a href="#" class="flex gap-3">
            <IconAskAI/>
            Ask AI
          </a>
        </li>
      </ul>
    </nav>

    <div
        class="text-white p-3 rounded-lg bg-slate-800 hover:bg-slate-700 transition-colors flex justify-between text-sm mx-6"
        v-if="isSidebarOpen">
      John Doe
      <IconChevronRight/>
    </div>

    <div class="text-gray-500 p-3 rounded-lg hover:bg-slate-800 transition-colors flex gap-3 text-sm m-6"
         v-if="isSidebarOpen">
      <IconLogOut/>
      Log out
    </div>
  </aside>
  <main class="flex-1 overflow-y-auto pl-12">
    <TheWelcome/>
    <p>
      Meow
    </p>
    <p>
      Meow
    </p>
    <p>
      Meow
    </p>
    <p>
      Meow
    </p>
    <p>
      Meow
    </p>
    <p>
      Meow
    </p>
    <p>
      Meow
    </p>
    <p>
      Meow
    </p>
    <p>
      Meow
    </p>
    <p>
      Meow
    </p>
    <p>
      Meow
    </p>
    <p>
      Meow
    </p>
    <p>
      Meow
    </p>
    <p>
      Meow
    </p>
    <p>
      Meow
    </p>
    <p>
      Meow
    </p>
    <p>
      Meow
    </p>
    <p>
      Meow
    </p>
    <p>
      Meow
    </p>
    <p>
      Meow
    </p>
    <p>
      Meow
    </p>
    <p>
      Meow
    </p>
    <p>
      Meow
    </p>
    <p>
      Meow
    </p>
    <p>
      Meow
    </p>
    <p>
      Meow
    </p>
    <p>
      Meow
    </p>
    <p>
      Meow
    </p>
    <p>
      Meow
    </p>
    <p>
      Meow
    </p>
    <p>
      Meow
    </p>
    <p>
      Meow
    </p>
    <p>
      Meow
    </p>
    <p>
      Meow
    </p>
    <p>
      Meow
    </p>
    <p>
      Meow
    </p>
    <p>
      Meow
    </p>
    <p>
      Meow
    </p>
    <p>
      Meow
    </p>
    <p>
      Meow
    </p>
    <p>
      Meow
    </p>
    <p>
      Meow
    </p>
    <p>
      Meow
    </p>
    <p>
      Meow
    </p>
  </main>
</template>
