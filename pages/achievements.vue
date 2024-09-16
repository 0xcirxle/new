<template>
  <div class="px-4 mt-12">
    <h2 class="text-2xl font-semibold">Achievements</h2>
  </div>
  <div class="mt-4" v-for="(achievement, i) in Achievements" :key="i">
    <div class="flex flex-row items-start justify-start w-full gap-4 ml-4">
      <div class="flex-shrink-0 w-10 h-10 mt-1">
        <img :src="achievement.image" :alt="achievement.title" class="w-full h-full object-cover rounded-lg" />
      </div>
      <div class="flex flex-col items-start justify-center w-full">
        <div class="text-lg font-semibold">{{ achievement.title }}</div>
        <div class="text-sm font-medium text-gray-400">
          <p>{{ achievement.year }}</p>
        </div>
        <div class="flex items-start mt-2">
          <div class="flex flex-col">
            <div v-for="(winner, index) in achievement.winners" :key="index" class="text-base">
              <div class="flex">
                <div class="flex flex-col items-center justify-center w-5 h-full gap-3 py-2 mr-4">
                  <div class="w-[8px] h-[8px] rounded-full bg-gray-300" />
                  <div v-if="index !== achievement.winners.length - 1" class="h-full min-h-[30px] border-r border-gray-300" />
                </div>
                {{ winner.description }}
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { Achievements } from "@/constants/achievements";
</script>
