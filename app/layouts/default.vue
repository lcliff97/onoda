<template>
  <div class="flex min-h-screen flex-col bg-stone text-ink">
    <SiteHeader />

    <main class="flex-1">
      <slot />
    </main>

    <SiteFooter />
  </div>
</template>
