<script setup lang="ts">
const SHAPES = [
  {
    icon: 'lucide:square',
    name: 'SQUARE',
  },
  {
    icon: 'lucide:diamond',
    name: 'DIAMOND',
  },
  {
    icon: 'lucide:circle',
    name: 'CIRCLE',
  },
]

const activePaintingType = ref('')
</script>

<template>
  <UCard variant="outline" class="w-48">
    <ToggleButtonGroup v-model="activePaintingType">
      <div class="flex flex-wrap items-center gap-2">
        <ToggleButton v-for="shape in SHAPES" :key="shape.name" :name="shape.name" :icon="shape.icon" />
      </div>
    </ToggleButtonGroup>
  </UCard>
</template>
