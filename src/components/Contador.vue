<template>
  <div class="contador">
    <h1>Desafio Contador Coderhouse</h1>
    <h2>{{contadorPadre}}</h2>
    <button v-on:click="aumenta()">+</button>
    <button v-on:click="resta()">-</button>
  </div>
</template>
<script>
export default {
  name: 'Contador',
  data() {
    return {
      contadorPadre: 0
    };
  },
  methods: {
    aumenta() {
      this.contadorPadre++;
    },
    resta() {
      this.contadorPadre--;
    }
  }
}
</script>
<style>

</style>
