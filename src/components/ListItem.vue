<script setup lang="ts">
import { NavigationMenuLink } from 'radix-vue'

const props = defineProps({
  title: String,
})
</script>

<template>
  <li>
    <NavigationMenuLink as-child>
      <a
        v-bind="$attrs"
        class="focus:shadow-[0_0_0_2px] focus:shadow-green7 border border-white hover:bg-theme-verylight hover:border hover:border-theme-gridlight block select-none p-3 text-[15px] leading-none no-underline outline-none transition-colors"
      >
        <div class="flex items-center mb-[5px] font-medium leading-[1.2]">
          <span class="inline-block pr-2">
            <slot name="icon"></slot>
          </span>
          <span>{{ props.title }}</span>
          
        </div>
        <p class="text-sm opacity-80 my-0 leading-[1.4]">
          <slot />
        </p>
      </a>
    </NavigationMenuLink>
  </li>
</template>