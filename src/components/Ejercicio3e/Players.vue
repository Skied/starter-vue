<template>
  <div>
    <select v-model="jugador" v-on:change="jugadorChange()">
      <option v-for="(value, key) in jugadores" :key="key" :value="value">{{value}}</option>
    </select>
  </div>

</template>
<script lang="ts">
import { Component, Vue, Emit } from 'vue-property-decorator';
import { EventBus } from '@/eventBus';

@Component
export default class PlayersComponent extends Vue {
  jugadores = {
    1: 'Pepito',
    2: 'Tronquito',
    3: 'Jaimito',
    4: 'Juanito'
  };
  jugador = '';

  // Forma directa
  // @Emit('change')
  // jugadorChange() {
  //   return this.jugador;
  // }

  // Forma indirecta
  jugadorChange() {
    EventBus.$emit('change', this.jugador);
  }
}
</script>
<style scoped lang="scss">

</style>