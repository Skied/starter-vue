<template>
  <div>
    <h3>Ejercicio 2A</h3>
    <input v-model="entero" type="number" min="0"/>
    <p>Resultado:</p>  
    <p>
    <span v-for="(value,index) in fibonacci" :key="index"
      v-bind:class="{'impar': value % 2 !== 0, 'par': value % 2 === 0}">{{value}}</span>
    </p>
    <button v-on:click="calcular()">Calcular</button>
    <button v-on:click="limpiar()">Limpiar</button>
  </div>
</template>
<script lang="ts">

import { Component, Vue } from 'vue-property-decorator';
@Component
export default class Ejercicio2a extends Vue {
  entero: number = 0;
  fibonacci: number[] = [0, 1];

  public calcular() {
    this.fibonacci = [0, 1];
    for( let i = 2; i <= this.entero; i++) {
      this.fibonacci.push(this.fibonacci[i-1]+ this.fibonacci[i-2]);
    }
  }

  public limpiar() {
    this.entero = 0;
    this.fibonacci = [0, 1];
  }

}

</script>
<style scoped lang="scss">
  span {
    margin-right: 5px;

    &.impar {
      color: red;
    }

    &.par {
      color: blue;
    }
  }
</style>