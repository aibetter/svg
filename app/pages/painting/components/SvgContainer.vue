<script setup lang="ts">
import type { VNode } from 'vue'

defineProps<{
  vnodes: VNode[]
}>()
</script>

<template>
  <svg xmlns="http://www.w3.org/2000/svg" width="1em" height="1em">
    <component :is="vnodes" />
  </svg>
</template>
