<script setup lang="ts">
import Sidebar from "@/components/Sidebar.vue";
import DashboardHeader from "@/components/DashboardHeader.vue";
import DashboardMain from "@/components/DashboardMain.vue";

import "@fontsource/rubik/400.css"
import "@fontsource/rubik/500.css"
import "@fontsource/rubik/600.css"
</script>

<template>
  <div class="flex h-screen font-rubik">
    <Sidebar/>

    <div class="flex flex-col w-full">
      <DashboardHeader/>

      <DashboardMain/>
    </div>
  </div>

</template>
