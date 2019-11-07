<template>
  <div>
    <b>Ejercicio 3D - Componente 2</b>
    <slot></slot>
  </div>
    
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component
export default class Ejercicio3d2 extends Vue {
    
}
</script>

<style scoped lang="scss">
  b {
    color: blue;
  }
</style>