<script lang="ts">
export const TOGGLE_BUTTON_GROUP_CONTEXT_KEY: InjectionKey<WritableComputedRef<string>> = Symbol('toggle-button-group')
</script>

<script setup lang="ts">
const model = defineModel<string>({
  required: true,
})

const activeName = computed({
  get() {
    return model.value
  },
  set(value) {
    model.value = value
  },
})

provide(TOGGLE_BUTTON_GROUP_CONTEXT_KEY, activeName)
</script>

<template>
  <div>
    <slot />
  </div>
</template>
