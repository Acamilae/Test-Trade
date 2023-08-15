<script setup>
import { Disclosure, DisclosureButton, DisclosurePanel } from "@headlessui/vue";
import { Bars3Icon, XMarkIcon } from "@heroicons/vue/24/outline";
import LoginDrown from "./LoginDrown.vue";
import EnglishDrown from "./EnglishDrown.vue";

const navigation = [
  { name: "FOREX", href: "#", current: true },
  { name: "STOCKS", href: "#", current: false },
  { name: "FUTURES", href: "#", current: false },
  { name: "TradeGATEHub", href: "#", current: false },
];
</script>

<template>
  <Disclosure as="nav" v-slot="{ open }">
    <div class="mx-2 px-2 sm:px-6 lg:px-6 py-6">
      <div
        class="relative flex h-16 items-center justify-center flex-col md:flex-row"
      >
        <div class="absolute inset-y-0 left-0 flex items-center sm:hidden">
          <!-- Mobile menu button-->
          <DisclosureButton
            class="relative inline-flex items-center justify-center rounded-md p-2 text-gray-400 hover:bg-gray-700 hover:text-white focus:outline-none focus:ring-2 focus:ring-inset focus:ring-white"
          >
            <span class="absolute -inset-0.5" />
            <span class="sr-only">Open main menu</span>
            <Bars3Icon
              v-if="!open"
              class="block h-6 w-6 text-white"
              aria-hidden="true"
            />
            <XMarkIcon
              v-else
              class="block h-6 w-6 text-white"
              aria-hidden="true"
            />
          </DisclosureButton>
        </div>
        <div class="flex flex-shrink-0 items-center">
          <img class="h-12 w-auto" src="../assets/Logo.svg" alt="Trade view" />
        </div>
        <div
          class="flex flex-1 items-center justify-center sm:items-stretch sm:justify-center"
        >
          <div class="hidden sm:ml-6 sm:block">
            <div class="flex space-x-4">
              <a
                v-for="item in navigation"
                :key="item.name"
                :href="item.href"
                :class="[
                  item.current ? 'text-white' : 'text-white  hover:text-white',
                  'rounded-md px-3 py-2 text-sm font-medium',
                ]"
                :aria-current="item.current ? 'page' : undefined"
                >{{ item.name }}</a
              >
            </div>
          </div>
        </div>
        <div
          class="flex items-center pr-2 sm:static sm:inset-auto sm:ml-6 sm:pr-0"
        >
          <LoginDrown />
          <span class="text-gray mx-1">|</span>
          <div class="flex justify-center items-center gap-5">
            <a href="#" class="text-gray pl-3">Contact Us</a>
            <EnglishDrown />
          </div>
        </div>
      </div>
    </div>

    <DisclosurePanel class="sm:hidden">
      <div class="space-y-1 px-2 pb-3 pt-2">
        <DisclosureButton
          v-for="item in navigation"
          :key="item.name"
          as="a"
          :href="item.href"
          :class="[
            item.current
              ? 'bg-gray-900 text-white'
              : 'text-gray-300 hover:bg-gray-700 hover:text-white',
            'block rounded-md px-3 py-2 text-base font-medium',
          ]"
          :aria-current="item.current ? 'page' : undefined"
          >{{ item.name }}</DisclosureButton
        >
      </div>
    </DisclosurePanel>
  </Disclosure>
</template>

<style></style>
