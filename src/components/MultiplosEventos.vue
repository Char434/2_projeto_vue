<template>
  <div>
    <button @click="primeiro('Primeiro evento'), segundo('Segundo evento'), terceiro()">
      Ativar múltiplos eventos
    </button>
    <p>{{ multiplos_eventos }}</p>
  </div>
</template>

<script setup>
import { ref } from 'vue'
let multiplos_eventos = ref('')
function primeiro(txt) {
  multiplos_eventos.value = txt
}
function segundo(txt) {
  setTimeout(() => (multiplos_eventos.value = txt), 500)
}
function terceiro(txt) {
  setTimeout(() => (multiplos_eventos.value = ''), 1000)
}
</script>

<style scoped>
div {
  margin: 100px;
}
</style>
