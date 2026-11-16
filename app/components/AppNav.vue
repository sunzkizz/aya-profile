<script setup lang="ts">
const links = [
  { to: '/', label: 'Home' },
  { to: '/profile', label: 'Profile' },
]
</script>

<template>
  <header class="border-b-4 border-denim bg-white">
    <nav
      class="mx-auto flex max-w-5xl items-center justify-between px-6 py-4"
      aria-label="Main navigation"
    >
      <NuxtLink to="/" class="font-display text-xl font-extrabold text-denim-deep">
        Aya<span class="text-lanyard">.</span>
      </NuxtLink>

      <ul class="flex gap-2">
        <li v-for="link in links" :key="link.to">
          <NuxtLink
            :to="link.to"
            class="rounded-full px-4 py-2 text-sm font-medium text-ink transition-colors hover:bg-paper focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-denim"
            exact-active-class="!bg-denim !text-white"
          >
            {{ link.label }}
          </NuxtLink>
        </li>
      </ul>
    </nav>
  </header>
</template>
