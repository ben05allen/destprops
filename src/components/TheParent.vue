<script setup lang="ts">
import { ref } from 'vue'
import SweetChildOfMine from './SweetChildOfMine.vue'

const msg = ref<string>('')

const changeMessage = () => {
  msg.value = 'children are to be seen and not heard'
}
</script>

<template>
  <div>
    <h2>Hi from parent</h2>
    <input type="text" v-model="msg" />
    <SweetChildOfMine :msg="msg" />
    <button @click="changeMessage">Change Message</button>
    <p>
      {{ msg }}
    </p>
  </div>
</template>
