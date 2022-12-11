<script setup>
import { ref } from "vue";
let number = ref(0);
let number2 = ref(0);

let result = ref(0);

function add() {
  result.value = parseInt(number.value) + parseInt(number2.value);
}

function subtract() {
  result.value = parseInt(number.value) - parseInt(number2.value);
}

function times() {
  result.value = parseInt(number.value) * parseInt(number2.value);
}

function divide() {
  result.value = parseInt(number.value) / parseInt(number2.value);
}
</script>

<template>
  <div>Calculator</div>
  <input type="text" v-model="number" />
  <input type="text" v-model="number2" />

  <div>
    <button @click="add">+</button>
    <button @click="subtract">-</button>
    <button @click="times">x</button>
    <button @click="times">/</button>
  </div>

  <div>Total: {{ result }}</div>
</template>

<style></style>
