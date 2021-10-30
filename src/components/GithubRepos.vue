
<script setup lang="ts">
import { reactive } from '@vue/reactivity'
import { useFetch } from '@vueuse/core'
import GithubRepoCard from './GithubRepoCard.vue'
import Gear from './Icons/Gear.vue'
const { data, isFetching } = useFetch('https://api.github.com/users/campino2k').get().json()

const user = reactive(data)

</script>

<template>
  <div v-if="!isFetching && data">
    <!--pre>{{ user }}</pre-->
    <div class="flex gap-3">
      <github-repo-card
        name="Repositories"
        :value="user.public_repos"
      />
      <github-repo-card
        name="Followers"
        :value="user.followers"
      />
    </div>
  </div>
  <div v-else class="flex justify-center items-center min-h-40">
    <Gear class="text-gray-500 animate-spin animate-duration-2000 text-5xl" />
  </div>
</template>
