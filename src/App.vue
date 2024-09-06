<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <p>{{ mensagem }}</p>
  <p>Contador: {{ contador }}</p>
  <button @click='incrementar'>Clique</button>
  <p v-if='exibir'>Texto visível</p>
  <p></p>
  <button @click='mostrar'>Clique para mostrar/ocultar texto</button>
  <p></p>
  <p>Lista não ordenada:</p>
  <ul>
    <li v-for="item in lista" :key="item">{{ item }}</li>
  </ul>
  <input v-model='nome' placeholder='Digite seu nome' />
  <p>Nome: {{ nome }}</p>
</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'

export default {
  data() {
    return {
      mensagem: 'Bem-vindo ao Vue.js!',
      contador: 0,
      exibir: false,
      lista: ['Escola', 'Trabalho', 'Academia', 'Casa'],
      nome: ''
    }
  },

  methods: { 
    incrementar() { 
      this.contador++; 
    },

    mostrar() {
      this.exibir = !this.exibir;
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

ul {
  list-style-type: none; /* Remove os marcadores */
  padding: 0; /* Remove o padding padrão */
  margin: 0; /* Remove a margem padrão */
}

ul li {
  padding: 10px 0; /* Adiciona espaçamento interno acima e abaixo */
}

ul li:not(:last-child) {
  border-bottom: 1px solid #ddd; /* Adiciona uma linha entre os itens */
}
</style>

<style scoped>
  p {color: red;}
</style>
