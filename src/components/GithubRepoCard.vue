<script setup lang="ts">
import { defineProps } from '@vue/runtime-core'

const props = defineProps<{
  name: string
  value: string | number
}>()
</script>

<template>
  <div
    class="border p-4 rounded-lg shadow-lg dark:shadow-light-900 grid"
    grid="row-auto gap-2"
  >
    <span
      font="bold"
    >
      {{ props.name }}
    </span>
    <hr>
    <span>
      {{ props.value }}
    </span>
  </div>
</template>
