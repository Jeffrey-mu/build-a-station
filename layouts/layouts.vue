<template>
  <main class="w-100vw h-100vh" flex="~ col">
    <LayoutsHeader />
    <div flex-1 overflow-auto>
      <LayoutsContent />
    </div>
    <LayoutsFooter />
    <slot />
  </main>
</template>
<script setup>
</script>
