<script setup lang="ts">
import { ref } from 'vue'
import SweetChildOfMine from './SweetChildOfMine.vue'

const count = ref<number>(0)

const increaseCount = () => {
  count.value++
}
</script>

<template>
  <div>
    <h2>Hi from parent</h2>
    <input type="number" v-model="count" />
    <SweetChildOfMine :count="count" />
    <button @click="increaseCount">Increase Count</button>
    <p>
      {{ count }}
    </p>
  </div>
</template>
