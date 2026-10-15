<script setup lang="ts">
import { onMounted, onUnmounted, ref } from "vue";

const isMenuOpen = ref(false);

let desktopQuery: MediaQueryList | undefined;

function handleViewportChange(event: MediaQueryListEvent) {
  if (event.matches) {
    isMenuOpen.value = false;
  }
}

onMounted(() => {
  desktopQuery = window.matchMedia("(min-width: 768px)");
  desktopQuery.addEventListener("change", handleViewportChange);
});

onUnmounted(() => {
  desktopQuery?.removeEventListener("change", handleViewportChange);
});
</script>

<template>
  <header
    class="relative flex items-center justify-between border-b border-ink/20 px-6 py-5 md:px-12"
  >
    <NuxtLink
      to="/"
      aria-label="ONODA home"
      class="font-display text-3xl tracking-wide"
      >ONODA<span class="text-vermilion">.</span></NuxtLink
    >

    <nav
      class="hidden md:flex items-center gap-6 text-xs font-semibold uppercase tracking-[0.2em]"
    >
      <NuxtLink
        to="/"
        class="transition-colors duration-200 hover:text-vermilion focus-visible:outline-2 focus-visible:outline-offset-4 focus-visible:outline-vermilion"
        >Home</NuxtLink
      >
      <NuxtLink
        to="/about"
        class="transition-colors duration-200 hover:text-vermilion focus-visible:outline-2 focus-visible:outline-offset-4 focus-visible:outline-vermilion"
        >About</NuxtLink
      >
      <NuxtLink
        to="/classes"
        class="transition-colors duration-200 hover:text-vermilion focus-visible:outline-2 focus-visible:outline-offset-4 focus-visible:outline-vermilion"
        >Classes</NuxtLink
      >
      <NuxtLink
        to="/coaches"
        class="transition-colors duration-200 hover:text-vermilion focus-visible:outline-2 focus-visible:outline-offset-4 focus-visible:outline-vermilion"
        >Coaches</NuxtLink
      >
      <NuxtLink
        to="/contact"
        class="transition-colors duration-200 hover:text-vermilion focus-visible:outline-2 focus-visible:outline-offset-4 focus-visible:outline-vermilion"
        >Contact</NuxtLink
      >
    </nav>
    <button
      type="button"
      class="md:hidden"
      :aria-label="
        isMenuOpen ? 'Close navigation menu' : 'Open navigation menu'
      "
      :aria-expanded="isMenuOpen"
      @click="isMenuOpen = !isMenuOpen"
    >
      {{ isMenuOpen ? "CLOSE" : "MENU" }}
    </button>
    <nav
      v-if="isMenuOpen"
      class="absolute left-0 top-full z-10 flex w-full flex-col gap-5 border-b border-ink/20 bg-stone px-6 py-6 md:hidden"
      aria-label="Mobile navigation"
    >
      <NuxtLink
        to="/"
        class="text-sm font-semibold uppercase tracking-[0.15em] transition-colors duration-200 hover:text-vermilion focus-visible:outline-2 focus-visible:outline-offset-4 focus-visible:outline-vermilion"
        @click="isMenuOpen = false"
        >Home</NuxtLink
      >
      <NuxtLink
        to="/about"
        class="text-sm font-semibold uppercase tracking-[0.15em] transition-colors duration-200 hover:text-vermilion focus-visible:outline-2 focus-visible:outline-offset-4 focus-visible:outline-vermilion"
        @click="isMenuOpen = false"
        >About</NuxtLink
      >
      <NuxtLink
        to="/classes"
        class="text-sm font-semibold uppercase tracking-[0.15em] transition-colors duration-200 hover:text-vermilion focus-visible:outline-2 focus-visible:outline-offset-4 focus-visible:outline-vermilion"
        @click="isMenuOpen = false"
        >Classes</NuxtLink
      >
      <NuxtLink
        to="/coaches"
        class="text-sm font-semibold uppercase tracking-[0.15em] transition-colors duration-200 hover:text-vermilion focus-visible:outline-2 focus-visible:outline-offset-4 focus-visible:outline-vermilion"
        @click="isMenuOpen = false"
        >Coaches</NuxtLink
      >
      <NuxtLink
        to="/contact"
        class="text-sm font-semibold uppercase tracking-[0.15em] transition-colors duration-200 hover:text-vermilion focus-visible:outline-2 focus-visible:outline-offset-4 focus-visible:outline-vermilion"
        @click="isMenuOpen = false"
        >Contact</NuxtLink
      >
    </nav>
  </header>
</template>
