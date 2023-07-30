<!-- eslint-disable vue/no-setup-props-destructure -->
<script setup lang="ts">
import { watch } from 'vue'

interface Props {
  count: number
}

// this fails for watching count
// defineProps<Props>()

// destructuring means a watcher can be used
const { count = 0 } = defineProps<Props>()

const evenOrOdd = (num: number): string => {
  return num % 2 === 0 ? 'even' : 'odd'
}

watch(
  () => count,
  () => {
    console.log(count)
  }
)
</script>

<template>
  <div style="background-color: aquamarine">
    <h2>hi from child</h2>
    <!-- <input type="text" v-model="propMsg" /> -->
    <p>{{ count }} is {{ evenOrOdd(count) }}</p>
  </div>
</template>
