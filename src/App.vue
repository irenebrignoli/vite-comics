<script>
import TheHeader from "./components/TheHeader.vue";

export default {
  methods: {},
  components: {
    TheHeader,
  },
};
</script>

<template>
  <TheHeader />
  <div class="debug-main">
    <div class="container">
      <h2>Content main here</h2>
    </div>
  </div>
</template>

<style lang="scss">
@use "./styles/general.scss";
@use "./styles/partials/mixins";

.debug-main {
  height: 150px;
  background-color: black;
  color: #fff;
  line-height: 150px;
}
</style>

<!-- 
  Descrizione:
Create un nuovo progetto utilizzando Vite e Vue 3 e definite i componenti necessari per strutturare il layout come da screenshot allegato.
Quando la struttura a macroblocchi è pronta, popolate le voci di menu dinamicamente usando i data del componente.
Per oggi diamo priorità alla struttura: quando è tutto bello solido, passiamo al Sass!
Bonus:
Creare un componente aggiuntivo per gestire la fascia azzurra con le icone.
 -->
