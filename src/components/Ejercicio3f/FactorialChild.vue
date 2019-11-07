<template>
  <div>Factorial de {{ n }}: {{ factorial }}</div>
</template>
<script lang="ts">
import { Vue, Component, Prop } from 'vue-property-decorator';

@Component
export default class FactorialChildComponent extends Vue {
  @Prop() n: number = 0;

  factorial: number = 1;

  calculo() {
    let num = this.n;
    this.factorial = 1;
    while(num > 0) {
      this.factorial *= num;
      num--;
    }
  }

  limpiar() {
    this.factorial = 1;
  }
}
</script>
<style scoped lang="scss">

</style>