<template>
  <div>
    <b>Ejercicio 3D - Componente 3</b>
    <slot></slot>
  </div>
    
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component
export default class Ejercicio3d3 extends Vue {
    
}
</script>

<style scoped lang="scss">
  b {
    color: green;
  }
</style>