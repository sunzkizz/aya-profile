<template>
  <div class="flex min-h-screen flex-col">
    <AppNav />
    <main class="mx-auto w-full max-w-5xl flex-1 px-6 pt-10">
      <slot />
    </main>
    <AppFooter />
  </div>
</template>
