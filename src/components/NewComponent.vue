<script setup lang="ts">
import { ref, onMounted } from 'vue'

const myName = ref({ Name: 'MK' })

myName.value.Name = 'DT'

const languages = ref<string[]>([])

onMounted(() => {
  languages.value = ['C#', 'JS']
})
</script>

<template>
  <ul>
    <li v-for="language in languages" :key="language">{{ language }}</li>
  </ul>

  <div>My new component: {{ myName.Name.toLocaleLowerCase() }}</div>

  <div></div>
</template>

<style scoped></style>
