<script setup>

import { ref } from 'vue'

let variableRef = ref(0);

let aux = ref(0);

let total = 1;

function factorial (variableRef){

  for(let i=1; i < variableRef +1; i++){

    total = total *i; 
  }

  return total;

}

function doClick() {


aux.value = variableRef.value;

}

</script>

<template>

  <div>
    <input v-model="variableRef" type="number">
    <button @click="doClick()" >PRESIONAME</button>
    <h1>{{ factorial(aux) }}</h1>
  </div>
  
</template>

<style scoped>

</style>
