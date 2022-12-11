<script setup>
import { ref } from "vue";
//  const ✅
//  let ✅
// @click ✅
// function ✅
let number = ref(0);

let items = ([1, 2, 3, 4, 5, 6, 7, 8, 9, 10,])

function increment(num) {
  number.value += num;
}

function decrement(num) {
  number.value -= num;
}

function message(message){
  alert(message)
}

</script>

<template>
  <div class="number">{{ number }}</div>
  <div class="wrapper">
    <button @click="increment(1)">Increment</button>
    <button @click="decrement(1)">Decrement</button>

    <button @click="message('ROBERT EDUARD')">Message 1</button>
    <button @click="message('REDSJ')">Message 2</button>

    <div>
      <div v-for="item in items" :key="items">
        <button @click="increment(item)">Incre{{item}}</button>
        <button @click="decrement(item)">Decre{{item}}</button>
      </div>
    </div>
  </div>
</template>

<style>
.number {
  color: white;
  font-size: 50px;
  font-weight: bold;
  margin-bottom: 20px;
  text-align: center;
  padding: 10px;
  background-color: green;
}

.wrapper {
  display: flex;
  grid-gap: 40px;
}
</style>
