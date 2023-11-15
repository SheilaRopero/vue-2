<script setup>
import { ref } from 'vue';

let tabla =ref(3)
let numeroInput ;
 let operacionErronea = ref(false)
 let numerofueradelRango = ref(false)

const calcular = ()=> {
  numeroInput +numeroInput
  if (numeroInput ==0 )  {
    operacionErronea.value = true;
  }

  if (numeroInput <0 ) {
    numeroInput = numeroInput*-1
  }

  if (numeroInput >= 1 && numeroInput<=100) {
    tabla.value = numeroInput
  }else{
    numerofueradelRango.value = true;
  }

}


</script>

<template>
  <h1>tabla de multiplicar</h1>
  <p>ingrese el numero a multiplicar</p>
   <input type="number" v-model="numeroInput"  >  <button @click="calcular" class="buton">calcular</button>
   <p  v-if="operacionErronea ==true">operacion prohibida</p>
   <p v-if="numerofueradelRango ==true">error! numero fuera del rango</p>
<div   >
<table>
  
  <tr>
    <td>Operacion</td>
    <td>resultado</td>
  </tr>

  <tr>
    <td>{{ tabla }} x 1 = </td>
    <td>{{ tabla * 1 }}</td>
  </tr>

  <tr>
    <td> {{ tabla }}x 2 = </td>
    <td>{{ tabla * 2 }}</td>
  </tr>

  <tr>
    <td>{{ tabla }} x 3 = </td>
    <td>{{ tabla * 3 }}</td>
  </tr>

  <tr>
    <td>{{ tabla }} x 4 = </td>
    <td>{{ tabla * 4 }}</td>
  </tr>

  <tr>
    <td>{{ tabla }} x 5 = </td>
    <td>{{ tabla * 5 }}</td>
  </tr>

  <tr>
    <td>{{ tabla }} x 6 = </td>
    <td>{{ tabla * 6 }}</td>
  </tr>

  <tr>
    <td>{{ tabla }} x 7 = </td>
    <td>{{ tabla * 7 }}</td>
  </tr>

  <tr>
    <td>{{ tabla }} x 8 = </td>
    <td>{{ tabla * 8 }}</td>
  </tr>

  <tr>
    <td>{{ tabla }} x 9 = </td>
    <td>{{ tabla * 9 }}</td>
  </tr>

  <tr>
    <td>{{ tabla }} x 10 = </td>
    <td>{{ tabla * 10 }}</td>
  </tr>
</table>

<div>

</div>

</div>
</template>

<style scoped>

.buton{
  margin-top: 12px;
  background-color: blueviolet;
  padding: 4px;
  border-radius: 12px;

}
</style>
