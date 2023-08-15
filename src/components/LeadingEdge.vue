<script setup>
import { ArrowTopRightOnSquareIcon } from "@heroicons/vue/24/outline";
</script>

<template>
  <div class="mx-auto max-w-7xl py-16 sm:px-6 lg:px-8">
    <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
      <!-- Columna de Texto -->
      <div class="flex flex-col justify-center">
        <h2 class="text-3xl font-bold mb-4">Leading Edge Technology</h2>
        <p class="font-light text-xl mb-14">
          Easy to use management tools, our fastest<br> possible execution and
          spreads as low as 0.0.
        </p>
        <a href="#" class="underline flex gap-1">
            Quick Guide: CommuniTraders Web User Manual
            <ArrowTopRightOnSquareIcon class="w-auto h-5"/>
        </a>
      </div>

      <!-- Columna de Imagen -->
      <div class="flex items-center justify-center">
        <img
          src="../assets/trade-view-pc.png"
          alt="Imagen"
          class="max-w-full h-auto"
        />
      </div>
    </div>
  </div>
</template>
