<script setup lang="ts">
import { TOGGLE_BUTTON_GROUP_CONTEXT_KEY } from './ToggleButtonGroup.vue'

const props = defineProps<{
  name: string
}>()

const activeName = inject(TOGGLE_BUTTON_GROUP_CONTEXT_KEY)

const model = defineModel<boolean>()

const asChildren = computed(() => props.name && activeName)

const isActive = computed(() => {
  if (asChildren.value) {
    return activeName!.value === props.name
  }

  return model.value
})

function onClick() {
  if (asChildren.value) {
    activeName!.value = props.name
  }
  else {
    model.value = !model.value
  }
}
</script>

<template>
  <UButton :variant="isActive ? 'solid' : 'ghost'" v-bind="$attrs" @click="onClick" />
</template>
