<template>
    <div>
        <h3>Ejercicio 3E</h3>
        <!-- Forma directa -->
        <!-- <player v-on:change="setearJugador($event)"></player> -->

        <!-- Forma indirecta -->
        <player></player>
        
        <p>Jugador: {{jugador}}</p>
    </div>
</template>
<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import PlayerComp from './Players.vue';
import { EventBus } from '@/eventBus';

@Component({
    components: {
        player: PlayerComp
    }
})
export default class SelectedPlayerComponent extends Vue {
    
  jugador: string = '';

  // Forma directa
  setearJugador(event: string) {
      this.jugador = event;
  }

  // Forma indirecta
  mounted() {
    EventBus.$on('change', (jug: string) => this.setearJugador(jug));
  }
}
</script>
<style scoped lang="scss">

</style>