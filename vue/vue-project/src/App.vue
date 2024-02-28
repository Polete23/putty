<template>
  <header>
    <div class="calculator">
      <div>
        <p>Haz clic en un número:</p>
        <div>
          <button v-for="num in numeros" :key="num" @click="mostrarNumero(num)">{{ num }}</button>
        </div>
        <div>
          <p v-if="numeroClicado !== null">Has clicado en el número: {{ numeroClicado }}</p>
        </div>
      </div>
    </div>
  </header>
</template>

<script setup>
const numeros = [1, 2, 3, 4, 5, 6, 7, 8, 9];
let numeroClicado = null;

const mostrarNumero = (numero) => {
  numeroClicado = numero;
  console.log(`Has clicado en el número: ${numero}`);
};
</script>

<style scoped>
.calculator {
  text-align: center;
}

.calculator button {
  padding: 10px 20px;
  margin: 5px;
  font-size: 18px;
  cursor: pointer;
}

.calculator button:hover {
  background-color: #eee;
}
</style>
