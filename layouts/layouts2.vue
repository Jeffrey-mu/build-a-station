<template>
  <main class="w-100vw h-100vh" flex="~ col">
    <Layouts2Header />
    <div flex-1 overflow-auto>
      <Layouts2Content />
    </div>
    <Layouts2Footer />
    <slot />
  </main>
</template>
<script setup>
</script>
