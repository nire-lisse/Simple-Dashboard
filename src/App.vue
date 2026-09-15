<script setup lang="ts">
import Sidebar from "@/components/Sidebar.vue";
import DashboardHeader from "@/components/DashboardHeader.vue";

import IconPlus from "@/components/icons/IconPlus.vue";
import IconLayout from "@/components/icons/IconLayout.vue";
import IconUser from "@/components/icons/IconUser.vue";
import IconArrowRight from "@/components/icons/IconArrowRight.vue";

import CreateOrderButton from "@/components/CreateOrderButton.vue";

import "@fontsource/rubik/500.css"
</script>

<template>
  <div class="flex h-screen">
    <Sidebar/>

    <div class="flex flex-col font-mono w-full">
      <DashboardHeader/>

      <main class="flex-1 overflow-y-auto p-8 gap-8">
        <header class="flex justify-between">
          <div>
            <h2 class="font-semibold text-3xl">
              Good morning, John!
            </h2>
            <h3 class="text-gray-500">
              Track orders, explore datasets, manage your team
            </h3>
          </div>
          <div>
            <CreateOrderButton/>
          </div>
        </header>

        <div class="flex my-10 justify-between gap-6">
          <div class="flex items-center p-6 border border-gray-300 rounded-xl gap-7 w-full">
            <div class="p-3 bg-emerald-100 rounded-md">
              <IconPlus/>
            </div>

            <div class="">
              <div class="font-bold ">
                Upload match
              </div>
              <div class="text-gray-500">
                Video file or link
              </div>
            </div>
          </div>

          <div class="flex items-center p-6 border border-gray-300 rounded-xl gap-7 w-full">
            <div class="p-3 bg-emerald-100 rounded-md">
              <IconLayout/>
            </div>

            <div class="">
              <div class="font-bold">
                Browser free datasets
              </div>
              <div class="text-gray-500">
                Free pre-processed matches
              </div>
            </div>
          </div>

          <div class="flex items-center p-6 border border-gray-300 rounded-xl gap-7 w-full">
            <div class="p-3 bg-emerald-100 rounded-md">
              <IconUser/>
            </div>

            <div class="">
              <div class="font-bold ">
                Invite team
              </div>
              <div class="text-gray-500">
                Add analysts & staff
              </div>
            </div>
          </div>
        </div>

        <table class="w-full border-collapse rounded-lg">
          <caption class="font-bold text-lg text-left p-4 border border-gray-300 rounded-t-lg">Orders</caption>

          <thead>
          <tr class="text-left text-gray-400 border border-gray-300">
            <th scope="col" class="py-4 pl-4">Match</th>
            <th scope="col">Author</th>
            <th scope="col">Other Date</th>
            <th scope="col">Status</th>
            <th scope="col">Data included</th>
            <th scope="col">Actions</th>
          </tr>
          </thead>

          <tbody>
          <tr class="border border-gray-300">
            <th scope="row" class="text-left p-4">
              <div class="">Arsenal vs Chelsea</div>
              <div class="text-gray-400">English Premier League - 12.02.2026</div>
            </th>
            <td>John Doe</td>
            <td>April 15</td>
            <td><span class="bg-emerald-100 rounded-full text-emerald-500 px-2 py-1">Done</span></td>
            <td>
              <ul class="text-gray-400 flex gap-4">
                <li>
                  Physical
                </li>
                <li>
                  Raw
                </li>
              </ul>
            </td>
            <td>
              <a href="#" class="flex gap-4">
                View
                <IconArrowRight/>
              </a>
            </td>
          </tr>

          <tr class="border border-gray-300">
            <th scope="row" class="text-left p-4">
              <div class="">Arsenal vs Chelsea</div>
              <div class="text-gray-400">English Premier League - 12.02.2026</div>
            </th>
            <td>John Doe</td>
            <td>April 15</td>
            <td><span class="bg-emerald-100 rounded-full text-emerald-500 px-2 py-1">Done</span></td>
            <td>
              <ul class="text-gray-400 flex gap-4">
                <li>
                  Physical
                </li>
                <li>
                  Raw
                </li>
              </ul>
            </td>
            <td>
              <a href="#" class="flex gap-4">
                View
                <IconArrowRight/>
              </a>
            </td>
          </tr>

          <tr class="border border-gray-300">
            <th scope="row" class="text-left p-4">
              <div class="">Arsenal vs Chelsea</div>
              <div class="text-gray-400">English Premier League - 12.02.2026</div>
            </th>
            <td>John Doe</td>
            <td>April 15</td>
            <td><span class="bg-orange-100 rounded-full text-orange-500 px-2 py-1">In progress</span></td>
            <td>
              <ul class="text-gray-400 flex gap-4">
                <li>
                  Physical
                </li>
                <li>
                  Raw
                </li>
              </ul>
            </td>
            <td>
              <a href="#" class="flex gap-4">
                View
                <IconArrowRight/>
              </a>
            </td>
          </tr>

          <tr class="border border-gray-300">
            <th scope="row" class="text-left p-4">
              <div class="">Arsenal vs Chelsea</div>
              <div class="text-gray-400">English Premier League - 12.02.2026</div>
            </th>
            <td>John Doe</td>
            <td>April 15</td>
            <td><span class="bg-orange-100 rounded-full text-orange-500 px-2 py-1">In progress</span></td>
            <td>
              <ul class="text-gray-400 flex gap-4">
                <li>
                  Physical
                </li>
                <li>
                  Raw
                </li>
              </ul>
            </td>
            <td>
              <a href="#" class="flex gap-4">
                View
                <IconArrowRight/>
              </a>
            </td>
          </tr>

          <tr class="border border-gray-300">
            <th scope="row" class="text-left p-4">
              <div class="">Arsenal vs Chelsea</div>
              <div class="text-gray-400">English Premier League - 12.02.2026</div>
            </th>
            <td>John Doe</td>
            <td>April 15</td>
            <td><span class="bg-red-100 rounded-full text-red-500 px-2 py-1">Declined</span></td>
            <td>
              <ul class="text-gray-400 flex gap-4">
                <li>
                  Physical
                </li>
                <li>
                  Raw
                </li>
              </ul>
            </td>
            <td>
              <a href="#" class="flex gap-4">
                View
                <IconArrowRight/>
              </a>
            </td>
          </tr>
          </tbody>
        </table>

      </main>

    </div>
  </div>

</template>
