<template>
  <footer class="border-t border-ink/20 px-6 py-8 md:px-12">
    <div
      class="flex flex-col gap-6 md:flex-row md:items-center md:justify-between"
    >
      <NuxtLink
        to="/"
        aria-label="ONODA home"
        class="font-display text-3xl tracking-wide"
        >ONODA<span class="text-vermilion">.</span></NuxtLink
      >

      <nav
        class="flex flex-wrap gap-x-6 gap-y-3 text-xs font-semibold uppercase tracking-[0.2em]"
        aria-label="Footer navigation"
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
    </div>

    <p class="mt-8 text-xs text-slate">
      &copy; {{ new Date().getFullYear() }} ONODA. All rights reserved.
    </p>
  </footer>
</template>
