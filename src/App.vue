<template>
  <div>
    <Ejercicio1a></Ejercicio1a>
    <Ejercicio1b></Ejercicio1b>
    <Ejercicio2a></Ejercicio2a>
    <Ejercicio3c></Ejercicio3c>
    <Ejercicio3d></Ejercicio3d>
  </div>
</template>

<script lang="ts">
import {Component, Vue} from 'vue-property-decorator';
import Ejercicio1aComponent from '@/components/Ejercicio1a.vue';
import Ejercicio1bComponent from '@/components/Ejercicio1b/Ejercicio1b.vue';
import Ejercicio2aComponent from '@/components/Ejercicio2a.vue';
import Ejercicio3cComponent from '@/components/Ejercicio3c.vue';
import Ejercicio3dComponent from '@/components/Ejercicio3d/Ejercicio3d.vue';
@Component({
  components: {
    Ejercicio1a: Ejercicio1aComponent,
    Ejercicio1b: Ejercicio1bComponent,
    Ejercicio2a: Ejercicio2aComponent,
    Ejercicio3c: Ejercicio3cComponent,
    Ejercicio3d: Ejercicio3dComponent,
  }
})
export default class App extends Vue {}
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
