<template>
  <div>
    <p>{{ compEmail }}</p>
    <p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
    <p v-else>Estou em busca de novas oportunidades!</p>
    <p>Utilizo as seguintes tecnologias para backend:</p>
    <ul>
      <li v-for="(technology, index) in backend_technologies" v-bind:key="index">
        {{ technology }}
      </li>
    </ul>
    <p>Utilizo as seguintes tecnologias para fron-end:</p>
    <ul>
      <li v-for="technology in frontend_technologies" :key="technology.id">
        {{ technology.language }}
      </li>
    </ul>
    <div>
      <button @click="showEmail">{{ textoBotao }}</button>
    </div>
    <p v-show="mostrar_email">Mande uma mensagem para: {{ email }}</p>
    <p>Para acessar meu portfólio <a :href="meu_link" target="__blank">basta clicar aqui</a></p>
    <Picture />
  </div>
</template>

<script setup>
import { ref } from 'vue'
import Picture from './Picture.vue'
let mostrar_email = ref(false)
let textoBotao = ref('Mostrar e-mail')
defineProps({ email: String, esta_trabalhando: Boolean })
const meu_link = ref('https://www.linkedin.com/in/miguel-souza-4833561a9/')
function showEmail() {
  mostrar_email.value = !mostrar_email.value
  if (!mostrar_email.value) {
    textoBotao.value = 'Mostrar e-mail'
  } else {
    textoBotao.value = 'Esconder e-mail'
  }
}
const backend_technologies = ref(['Javascript', 'PHP', 'Laravel'])
const frontend_technologies = ref([
  { id: 1, language: 'HTML' },
  { id: 2, language: 'CSS' },
  { id: 3, language: 'Vue' },
])
</script>
