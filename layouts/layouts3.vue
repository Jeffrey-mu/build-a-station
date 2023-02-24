<template>
  <main class="w-100vw h-100vh" flex="~ col">
    <Layouts3Header />
    <div flex-1 overflow-auto>
      <slot />
    </div>
    <Layouts3Footer />
  </main>
</template>
<script setup>
</script>
