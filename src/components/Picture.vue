<template>
  <img :src="avatar" :alt="descricao" />
  <!-- os : significam que estou usando o v-bind, alocando as propriedades dinamicamente -->
  <MudarImagem @mudar-imagem="trocarImagem" />
</template>

<script setup>
import { ref } from 'vue'
import MudarImagem from './MudarImagem.vue'
let avatar = ref('/img/avatar.png')
const descricao = ref('Miguel Lima')
function trocarImagem() {
  avatar.value = '/img/avatar2.png'
}
</script>
