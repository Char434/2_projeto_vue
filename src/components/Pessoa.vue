<template>
  <div>
    <h2>Esta é a descrição da pessoa: {{ nome }}</h2>
    <Info :email="email" :esta_trabalhando="true" />
    <!-- o email que está em data seria enviado via props para o componente -->
    <Form />
  </div>
</template>

<script setup>
import { ref } from 'vue'
import Info from './Info.vue'
import Form from './Form.vue'
const nome = ref('Miguel')
const email = ref('mslima434@gmail.com')
</script>
