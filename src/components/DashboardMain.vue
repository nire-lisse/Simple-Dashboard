<script setup lang="ts">
import IconPlus from "@/assets/icons/Plus.svg";
import IconLayout from "@/assets/icons/Dataset.svg";
import IconUser from "@/assets/icons/User.svg";

import CreateOrderButton from "@/components/CreateOrderButton.vue";
import MainButton from "@/components/MainButton.vue";
import TableLine from "@/components/TableLine.vue";
</script>

<template>
  <main class="flex-1 flex flex-col overflow-y-auto p-9 pb-0 gap-8">
    <header class="flex justify-between">
      <div>
        <h2 class="font-semibold text-2xl text-[#272C43]">
          Good morning, John!
        </h2>
        <div class="text-[#9399AF] font-normal">
          Track orders, explore datasets, manage your team
        </div>
      </div>
      <div>
        <CreateOrderButton/>
      </div>
    </header>

    <div class="flex flex-col w-full gap-4">
      <div class="flex justify-between gap-4 text-sm">
        <MainButton>
          <template #icon>
            <IconPlus/>
          </template>
          <template #h1>
            Upload match
          </template>
          <template #h2>
            Video file or link
          </template>
        </MainButton>

        <MainButton>
          <template #icon>
            <IconLayout/>
          </template>
          <template #h1>
            Browser free datasets
          </template>
          <template #h2>
            Free pre-processed matches
          </template>
        </MainButton>

        <MainButton>
          <template #icon>
            <IconUser/>
          </template>
          <template #h1>
            Invite team
          </template>
          <template #h2>
            Add analysts & staff
          </template>
        </MainButton>
      </div>

      <table class="w-full bg-white border-[#E9EBEF]">
        <caption
            class="font-semibold text-left py-3 pl-6 border border-[#E9EBEF] rounded-t-lg text-[#272C43] border-b-0">
          <div class="h-7.5 flex items-center">Orders</div>
        </caption>

        <thead>
        <tr class="text-left text-[#9399AF] border border-[#E9EBEF] bg-[#F9FBFC] h-12 text-xs">
          <th scope="col" class="pl-6">Match</th>
          <th scope="col">Author</th>
          <th scope="col">Other Date</th>
          <th scope="col">Status</th>
          <th scope="col">Data included</th>
          <th scope="col">Actions</th>
        </tr>
        </thead>

        <tbody class="divide-y divide-[#E9EBEF] border border-[#E9EBEF]">
        <TableLine status="Done">
          <template #Data>
            <ul class="flex gap-2.5">
              <li class="py-1 px-2">Physical</li>
              <li class="py-1 px-2">Raw</li>
            </ul>
          </template>
        </TableLine>

        <TableLine status="Done">
          <template #Data>
            <ul class="flex gap-2.5">
              <li class="py-1 px-2">Physical</li>
              <li class="py-1 px-2">Raw</li>
            </ul>
          </template>
        </TableLine>

        <TableLine status="In progress">
          <template #Data>
            <ul class="flex gap-2.5">
              <li class="py-1 px-2">Physical</li>
              <li class="py-1 px-2">Raw</li>
            </ul>
          </template>
        </TableLine>

        <TableLine status="In progress">
          <template #Data>
            <ul class="flex gap-2.5">
              <li class="py-1 px-2">Physical</li>
              <li class="py-1 px-2">Raw</li>
            </ul>
          </template>
        </TableLine>

        <TableLine status="Declined">
          <template #Data>
            —
          </template>
        </TableLine>
        </tbody>
      </table>
    </div>
  </main>
</template>

<style scoped>

</style>