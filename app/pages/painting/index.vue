<script setup lang="ts">
import Canvas from './components/Canvas.vue'
import Header from './components/Header.vue'
import PlaintBox from './components/PlaintBox.vue'
import Refinement from './components/Refinement.vue'
</script>

<template>
  <div>
    <Header />
    <main class="h-[calc(100vh-3.5rem)] relative">
      <Canvas class="size-full" />
      <PlaintBox class="absolute top-4 left-4" />
      <Refinement class="absolute top-4 right-4" />
    </main>
  </div>
</template>
