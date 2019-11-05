<template>
  <div>
    <h3>Ejercicio 3C</h3>

    <input v-model="text"/>
    <input type="number" min="0" v-model="maxLength"/>

    <p>{{texto}}</p>
  </div>
</template>
<script lang="ts">

import { Component, Vue, Mixins } from 'vue-property-decorator';

@Component
class TextCounter extends Vue {
  text: string = '';
  maxLength: number = 5;

  get texto() {
    if (this.text.length < this.maxLength) {
      return this.text;
    }
    return this.text.substring(0, this.maxLength).concat('...');
  }
}

@Component
export default class Ejercicio3c extends Mixins(TextCounter) {
  constructor() {
    super();
    this.text = 'Hola, Buenos días';
  }
}

</script>
<style scoped lang="scss">
</style>