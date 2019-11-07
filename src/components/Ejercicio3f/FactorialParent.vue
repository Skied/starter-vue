<template>
  <div>
    <h3>Ejercicio 3F</h3>
    <input type="number" v-model="numero" min="0"/>
    <factorial :n="numero" ref="child"></factorial>
    <button @click="calcular()">Calcular</button>
    <button @click="limpiar()">Limpiar</button>
  </div>
</template>

<script lang="ts">
import { Vue, Component, Prop, Ref } from 'vue-property-decorator';
import FactorialChild from './FactorialChild.vue';

@Component({
  components: {
    factorial: FactorialChild
  }
})
export default class FactorialParentComponent extends Vue {
  numero: number = 0;

  @Ref('child') readonly child!: FactorialChild;

  calcular() {
    this.child.calculo();
  }

  limpiar() {
    this.numero = 0;
    this.child.limpiar();
  }
}
</script>
<style scoped lang="scss">

</style>