<script setup>



// Lógica do componente
//   export default {
// data() {
// return {
//   contador: 10
//   }
// },
// methods: {
//  incrementarContador() {
//   this.contador++
//   },
//  decrementarContador() {
//    this.contador--
//   }
//  },
// resetar(){
// this.contador = 0
//   },
//  mounted() {
//   console.log(`O valor inicial do contador é ${this.contador}.`)
//  }
// }
//

import { onMounted, ref } from 'vue'
const contador = ref(10)
function incrementar() {
  contador.value++
  console.log(contador.value)
} function decrementar() {
  if (contador.value > 0) {
    contador.value--
  }
} function resetar() {
  contador.value = 0
} onMounted(() => {
  console.log('Componente montado')
  console.log('Contador: ' + contador.value)
})
</script>

<template>
  <!-- Template do componente baseado em HTML -->
  <button @click="incrementar">+</button>
  <button @click="decrementarContador">-</button>
  <button @click="resetar">C</button>
  <p>Valor do contador é: {{ contador }}</p>
</template>

<style escoped>
/* Estilos do componente baseado em CSS */
button {
  font-weight: bold;
}
</style>