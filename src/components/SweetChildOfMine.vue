<script setup lang="ts">
interface Props {
  msg: string
}

// const { msg = 'hello world' } = defineProps<Props>()
const _ = defineProps<Props>()
</script>

<template>
  <div style="background-color: aquamarine">
    <h2>hi from sweet child of mine</h2>
    <!-- <input type="text" v-model="propMsg" /> -->
    <p>{{ msg }}</p>
  </div>
</template>
