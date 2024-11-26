<template>
  <div><button @click="$emit('mudarImagem')">Trocar imagem de perfil</button></div>
</template>

<script setup>
defineEmits(['mudarImagem'])
</script>
