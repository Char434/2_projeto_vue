<template>
  <div>
    <Header :esta_logado="true" />
    <PrimeiroComponente />
    <p>O dado de app é: {{ testando }}</p>
    <LifeCycle />
    <Pessoa />
  </div>
</template>

<script setup>
import Header from './components/Header.vue'
import PrimeiroComponente from './components/PrimeiroComponente.vue'
import LifeCycle from './components/LyfeCycle.vue'
import Pessoa from './components/Pessoa.vue'

import { ref } from 'vue'
const testando = ref('teste')
</script>

<style>
body {
  background-color: #333;
  color: #fff;
}
a {
  color: red;
}
</style>
