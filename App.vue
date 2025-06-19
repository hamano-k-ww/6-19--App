<script setup>
import { ref } from "vue";

const display = ref([]);
function Number(number) {
  display.value.push(number);
}

function clearDisplay() {
  display.value = [];
}

function changeSign() {
  display.value = display.value.map((num) => -num);
}
</script>

<template>
  <h1>計算機App</h1>
  <div>
    <button @click="clearDisplay" class="clear-button">AC</button>
    <button @click="changeSign" class="clear-button">+/-</button>
  </div>
  <div>
    <button @click="Number(7)" class="add-button">7</button>
    <button @click="Number(8)" class="add-button">8</button>
    <button @click="Number(9)" class="add-button">9</button>
  </div>
  <div>
    <button @click="Number(4)" class="add-button">4</button>
    <button @click="Number(5)" class="add-button">5</button>
    <button @click="Number(6)" class="add-button">6</button>
  </div>
  <div>
    <button @click="Number(1)" class="add-button">1</button>
    <button @click="Number(2)" class="add-button">2</button>
    <button @click="Number(3)" class="add-button">3</button>
  </div>
</template>

<style></style>
