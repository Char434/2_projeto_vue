<template>
  <h1>Meu nome é: {{ nome }}</h1>
</template>

<script setup>
import { ref, onMounted, onUnmounted, onUpdated } from 'vue'
const nome = ref('Ainda não sei')

onMounted(() => {
  setTimeout(() => {
    nome.value = 'Miguel'
  }, 1000)
  lifCycle()
})
function lifCycle() {
  console.log('executou')
}
</script>
