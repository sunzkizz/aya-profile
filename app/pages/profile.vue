<script setup lang="ts">
useHead({ title: 'Profile | Aya' })

// Edit the details below to update the page.
const personalInfo = [
  { label: 'Full name', value: 'Sofia May M. Esmaya' },
  { label: 'Nickname', value: 'Aya' },
  { label: 'Age', value: '21 years old' },
  { label: 'Birthday', value: 'May 29, 2005' },
  { label: 'Email & Mobile No.', value: 'itsAyasmme@gmail.com / 09635712950' },
  { label: 'Program', value: 'Bachelor of Science in Information Technology' },
]

const education = [
  {
    school: 'Caraga State University',
    detail: 'BS Information Technology',
    note: 'Currently enrolled',
  },
]

const skills = [
  'Communication Skills',
  'Leadership Skills',
  'Creative Arts',
  'Basic Vue & Nuxt',
  'Basic OpenCV',
  'Figma',
]

const interests = [
  'Computer vision',
  'Frontend Development',
  'Web development',
]

const hobbies = [
  'Building side projects for fun',
  'Reading books',
  'Listening to Music or Watching movies',
  'Painting and Journaling',
]
</script>

<template>
  <div>
    <header class="flex flex-col items-center gap-6 sm:flex-row">
      <img
        src="/aya.jpg"
        alt="Portrait of Aya"
        class="h-32 w-32 rounded-full border-4 border-denim object-cover object-top"
        width="128"
        height="128"
      >
      <div class="text-center sm:text-left">
        <h1 class="font-display text-4xl font-extrabold text-denim-deep">My Profile</h1>
        <p class="mt-1 text-lg text-ink/80">Sofia May M. Esmaya, but you can call me Aya.</p>
      </div>
    </header>

    <div class="mt-12 grid gap-8 md:grid-cols-2">
      <section class="rounded-2xl bg-white p-6 shadow-sm md:col-span-2">
        <h2 class="font-display text-2xl font-bold text-denim-deep">Personal information</h2>
        <dl class="mt-4 grid gap-x-8 gap-y-4 sm:grid-cols-2">
          <div v-for="item in personalInfo" :key="item.label">
            <dt class="text-sm text-ink/60">{{ item.label }}</dt>
            <dd class="font-medium">{{ item.value }}</dd>
          </div>
        </dl>
      </section>

      <section class="rounded-2xl bg-white p-6 shadow-sm">
        <h2 class="font-display text-2xl font-bold text-denim-deep">Educational background</h2>
        <ul class="mt-4 space-y-4">
          <li
            v-for="item in education"
            :key="item.school"
            class="border-l-4 border-lanyard pl-4"
          >
            <p class="font-medium">{{ item.school }}</p>
            <p class="text-ink/80">{{ item.detail }}</p>
            <p class="text-sm text-ink/60">{{ item.note }}</p>
          </li>
        </ul>
      </section>

      <section class="rounded-2xl bg-white p-6 shadow-sm">
        <h2 class="font-display text-2xl font-bold text-denim-deep">Hobbies</h2>
        <ul class="mt-4 list-disc space-y-2 pl-5 marker:text-amber">
          <li v-for="hobby in hobbies" :key="hobby">{{ hobby }}</li>
        </ul>
      </section>

      <section class="rounded-2xl bg-white p-6 shadow-sm md:col-span-2">
        <h2 class="font-display text-2xl font-bold text-denim-deep">Skills and interests</h2>

        <h3 class="mt-4 text-sm font-medium text-ink/60">Skills</h3>
        <ul class="mt-2 flex flex-wrap gap-2">
          <li
            v-for="skill in skills"
            :key="skill"
            class="rounded-full bg-denim px-4 py-1.5 text-sm font-medium text-white"
          >
            {{ skill }}
          </li>
        </ul>

        <h3 class="mt-6 text-sm font-medium text-ink/60">Interests</h3>
        <ul class="mt-2 flex flex-wrap gap-2">
          <li
            v-for="interest in interests"
            :key="interest"
            class="rounded-full bg-amber/30 px-4 py-1.5 text-sm font-medium text-denim-deep"
          >
            {{ interest }}
          </li>
        </ul>
      </section>
    </div>

    <div class="mt-10">
      <NuxtLink
        to="/"
        class="inline-block rounded-full border-2 border-denim px-6 py-3 font-medium text-denim transition-colors hover:bg-denim hover:text-white focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-denim"
      >
        Back to home
      </NuxtLink>
    </div>
  </div>
</template>
