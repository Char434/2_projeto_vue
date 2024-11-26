<template>
  <div>
    <h2>Meu formulário:</h2>
    <form action="" @submit.prevent="enviarFormulario()">
      <div>
        <InputText />
      </div>
      <div>
        <InputText />
      </div>
      <div>
        <Submit />
      </div>
    </form>
    <p>Conteúdo</p>
    <p>Conteúdo</p>
    <p>Conteúdo</p>
  </div>
</template>

<script setup>
import InputText from './form/InputText.vue'
import Submit from './form/Submit.vue'

function enviarFormulario() {
  console.log('formulário enviado')
}
</script>

<style scoped>
p {
  margin: 150px;
}
</style>
