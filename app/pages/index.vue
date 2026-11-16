<script setup lang="ts">
useHead({ title: 'Home | Aya' })
const { baseURL } = useRuntimeConfig().app
</script>

<template>
  <section class="grid items-center gap-12 md:grid-cols-[1.1fr_0.9fr]">
    <div>
      <p class="mb-3 inline-block rounded-full bg-amber/30 px-4 py-1 text-sm font-medium text-denim-deep">
        Welcome to my short profile
      </p>

      <h1 class="font-display text-5xl font-extrabold leading-tight text-denim-deep sm:text-6xl">
        Hi! I'm Aya
      </h1>

      <p class="mt-2 font-display text-2xl font-medium text-ink/80">
        Sofia May M. Esmaya
      </p>

      <p class="mt-6 max-w-md text-lg leading-relaxed">
        I'm a 21 years old BSIT student in Caraga State University. I love creative arts and spend most of my time painting, 
        watching films, and extracurricular activities like org works. 
        I love taking different tasks and roles that will challenge my skills and makes me learn more.
      </p>

      <div class="mt-8 flex flex-wrap gap-3">
        <NuxtLink
          to="/profile"
          class="rounded-full bg-denim px-6 py-3 font-medium text-white transition-colors hover:bg-denim-deep focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-denim"
        >
          View my profile
        </NuxtLink>
      </div>
    </div>

    <div class="relative mx-auto w-full max-w-sm">
      <div class="absolute -bottom-4 -right-4 h-full w-full rounded-[2rem] bg-denim" aria-hidden="true" />
      <div class="absolute -left-3 top-8 h-24 w-3 rounded-full bg-lanyard" aria-hidden="true" />
      <img
        :src="`${baseURL}aya.jpg`"
        alt="Aya smiling and winking, wearing a denim jacket and amber-tinted glasses"
        class="relative aspect-[4/5] w-full rounded-[2rem] object-cover"
        width="900"
        height="1125"
      >
    </div>
  </section>
</template>
