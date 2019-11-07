<template>
  <div>
    <h3>Ejercicio 3D</h3>

    <div class="selector">
      <span>Seleccione:</span>
      <select v-model="currentComponent">
        <option v-for="(value, index) in opciones" :key="index" v-bind:value="value.component">
          {{value.texto}}
        </option>
      </select>
      <input v-model="texto" type="text"/>
    </div>

    <div>
      <component v-bind:is="currentComponent">
        <div>{{texto}}</div>
      </component>
    </div>
  </div>
    
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import Ejercicio3d1 from './Ejercicio3d-1.vue';
import Ejercicio3d2 from './Ejercicio3d-2.vue';
import Ejercicio3d3 from './Ejercicio3d-3.vue';

@Component
export default class DynamicComponent extends Vue {
    opciones: any[] = [
      { texto: 'Componente 1', component: Ejercicio3d1 },
      { texto: 'Componente 2', component: Ejercicio3d2 },
      { texto: 'Componente 3', component: Ejercicio3d3 },
    ];

    texto: string = 'Placeholder';

    currentComponent = Ejercicio3d1;
}
</script>

<style scoped lang="scss">
.selector {
  display: flex;
}

</style>