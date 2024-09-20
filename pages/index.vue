<script setup>
import signature from '@/assets/tusi/tusi-tattoo.svg?raw'
</script>

<template>
  <main class="flex flex-col min-h-screen relative">
    <section class="flex grow overflow-clip">
      <div class="-top-20 background animate w-screen h-56" />
      <div class="-top-6 background w-screen h-56" />
      <div class="top-10 background w-screen h-56" />
      <div class="top-10 background animate-left w-screen h-56" />
      <div class="top-24 right-2 background w-screen h-56" />
      <div class="top-40 background w-screen h-56" />
      <div class="top-40 background animate w-screen h-56" />
      <div class="container mx-auto flex flex-col justify-center items-center">
        <div class="md:w-[900px] sm:w-[700px] max-sm:w-[500px]" v-html="signature" />
      </div>
      <div class="-bottom-20 background animate-left w-screen h-56 -translate-y-10" />
      <div class="-bottom-6 background w-screen h-56" />
      <div class="bottom-10 left-2 background w-screen h-56" />
      <div class="bottom-10 background animate w-screen h-56" />
      <div class="bottom-24 background w-screen h-56" />
      <div class="bottom-40 right-4 background w-screen h-56" />
      <div class="bottom-40 background animate-left w-screen h-56" />
    </section>
  </main>
</template>

<style lang="scss" scoped>
$bg-url: "@/assets/tusi/tusi-tattoo-back.svg";

.background {
  background: url($bg-url);
  position: fixed;
  width: 2 * 100vw;
}

.animate {
  animation: bg-scrolling 17s linear infinite;
}
@keyframes bg-scrolling {
  from {
     transform: translateX(-50%);
   }
   to {
     transform: translateX(0%);
   }
}
// Left
.animate-left {
  animation: bg-scrolling-left 17s linear infinite;
}
@keyframes bg-scrolling-left {
  from {
     transform: translateX(0%);
   }
   to {
     transform: translateX(-50%);
   }
}
</style>
