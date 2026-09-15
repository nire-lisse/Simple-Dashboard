<script setup lang="ts">
import IconChevronLeft from "@/assets/icons/ChevronLeft.svg";
import IconChevronRight from "@/assets/icons/ChevronRight.svg";
import IconHome from "@/assets/icons/Home.svg";
import IconTrophy from "@/assets/icons/Trophy.svg";
import IconDataset from "@/assets/icons/Dataset.svg";
import IconSettings from "@/assets/icons/Settings.svg";
import IconAskAI from "@/assets/icons/AskAI.svg";
import IconLogOut from "@/assets/icons/LogOut.svg";
import Logo from "@/assets/icons/Logo.svg"

import CreateOrderButton from "@/components/CreateOrderButton.vue";

import {ref} from "vue";
import SidebarButton from "@/components/SidebarButton.vue";

const isSidebarOpen = ref(true);

function toggleSidebar() {
  isSidebarOpen.value = !isSidebarOpen.value;
}
</script>

<template>
  <aside
      class="bg-[#0C0F21] shrink-0 flex flex-col transition-all duration-300 overflow-hidden px-3 py-6 gap-6 font-medium text-xs"
      :class="isSidebarOpen ? 'w-50' : 'w-10'">
    <header class="pb-5 pl-3 flex justify-between items-center border-b border-[#1D233B]">
      <Logo/>

      <button
          class="flex items-center justify-center size-5 bg-[#1B213B] rounded-sm cursor-pointer hover:bg-slate-700 transition-colors"
          @click="toggleSidebar">
        <IconChevronLeft v-if="isSidebarOpen" class="size-3"/>
        <IconChevronLeft v-else class="size-3 rotate-180"/>
      </button>

    </header>

    <CreateOrderButton v-if="isSidebarOpen"/>

    <nav class="flex justify-center h-full" v-if="isSidebarOpen">
      <ul class="space-y-1 w-full">
        <li>
          <SidebarButton active>
            <template #icon>
              <IconHome/>
            </template>
            <template #text>Dashboard</template>
          </SidebarButton>
        </li>
        <li>
          <SidebarButton text-color="#FFB200">
            <template #icon>
              <IconTrophy/>
            </template>
            <template #text>World Cup 2026</template>
          </SidebarButton>
        </li>
        <li>
          <SidebarButton>
            <template #icon>
              <IconDataset/>
            </template>
            <template #text>Free datasets</template>
          </SidebarButton>
        </li>
        <li>
          <SidebarButton>
            <template #icon>
              <IconSettings/>
            </template>
            <template #text>Settings</template>
          </SidebarButton>
        </li>
        <li>
          <SidebarButton>
            <template #icon>
              <IconAskAI/>
            </template>
            <template #text>Ask AI</template>
          </SidebarButton>
        </li>
      </ul>
    </nav>

    <div class="flex flex-col gap-3">
      <a href="#"
         class="text-white px-4 py-3 rounded-lg bg-[#181C32] hover:bg-slate-700 transition-colors flex justify-between"
         v-if="isSidebarOpen">
        John Doe
        <IconChevronRight/>
      </a>

      <a href="#" class="text-[#9399AF] p-3 rounded-lg hover:bg-slate-800 transition-colors flex gap-3 text-sm"
         v-if="isSidebarOpen">
        <IconLogOut/>
        Log out
      </a>
    </div>
  </aside>
</template>

<style scoped>

</style>