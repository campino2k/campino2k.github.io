
<script setup lang="ts">

import { useFetch } from '@vueuse/core'

const { data } = useFetch('https://api.github.com/users/campino2k')

// eslint-disable-next-line no-console
console.log(data)

</script>

<template>
  <div>
    ohai. this is repos
  </div>
</template>
