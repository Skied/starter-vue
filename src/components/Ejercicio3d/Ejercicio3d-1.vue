<template>
  <div>
    <b>Ejercicio 3D - Componente 1</b>
    <slot></slot>
  </div>
    
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component
export default class Ejercicio3d1 extends Vue {
    
}
</script>

<style scoped lang="scss">
  b {
    color: red;
  }
</style>