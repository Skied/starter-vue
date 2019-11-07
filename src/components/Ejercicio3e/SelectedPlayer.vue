<template>
    <div>
        <h3>Ejercicio 3E</h3>
        <player v-on:change="setearJugador($event)"></player>
        <p>Jugador: {{jugador}}</p>
    </div>
</template>
<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import PlayerComp from './Players.vue';

@Component({
    components: {
        player: PlayerComp
    }
})
export default class SelectedPlayerComponent extends Vue {
    
    jugador: string = '';

    setearJugador(event: string) {
        this.jugador = event;
    }
}
</script>
<style scoped lang="scss">

</style>