<script setup lang="ts">
import { defineProps } from '@vue/runtime-core'

const props = defineProps<{
  name: string
  value: string | number
}>()
</script>

<template>
  <div>
    <span>
      {{ props.name }}
    </span>
    <hr>
    <span>
      {{ props.value }}
    </span>
  </div>
</template>
