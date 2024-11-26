<template>
  <div>
    <button @click="ativar">Clique aqui</button>
    <span v-show="ativou">Ativado!</span>
  </div>
</template>

<script setup>
import { ref } from 'vue'
let ativou = ref(false)

function ativar() {
  ativou.value = !ativou.value
}
</script>
