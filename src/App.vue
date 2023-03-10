<script setup>
import { ref } from 'vue';

    const nome = 'Maria Eduarda'
    const idade = 16
    const numero = 15
    const valor1 = 0
    const valor2 = 0
    valor1 = ref()
    valor2 = ref()
    function inverter(texto) {
        return texto.split('').reverse().join('')
    }

    function saudacao() {
        return `Olá, ${nome}!`
    }
</script>

<template>
    <div class="info">
        <h1>Exemplo 1 - Mostrando informações na tela</h1>
        <p>Nome: {{ nome }} </p>
        <p>Idade: {{ idade }}  anos</p>
        <hr />
        <p>Para completar 50 anos faltam: {{ 50 - idade }}  anos</p>
        <p>O nome tem {{ nome.length }}  caracteres</p>
        <p>O nome invertido é: {{ inverter(nome) }} </p>
        <hr />
        <p> Exemplo de saudação usando função</p>
        <p> {{ saudacao() }}  </p>
        <hr />
        <p> o numero é {{ numero }} e o seu dobro é: {{ 2 * numero }}</p>
        <p><input v-model="valor1" /></p>
        <p><input v-model="valor2" /></p>
        <p>A soma dos números acima é {{ valor1 + valor2 }}</p>
     </div>
</template>

<style scoped>
.info {
  background-color: rgba(35,12,22,1);
  padding: 20px 30px;
  color: rgb(183, 210, 219);
  border-radius: 10px;
}

h1 {
  color: white;
  font-weight: bold;
  font-size: 1.5em;
}
</style>