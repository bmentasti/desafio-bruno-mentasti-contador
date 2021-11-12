<template>
  <div class="contador">
    <h1>Desafio Contador Coderhouse</h1>
    <h2>{{contadorPadre}}</h2>
    <button v-on:click="aumenta()">+</button>
    <button v-on:click="resta()">-</button>
    <button v-on:click="multi()">*</button>
    <button class="reset" @click="reset">Reset</button>
    <br>
    <p>La Cantidad de clicks totales es de <b>Suma</b> {{ sumar }}</p>
    <p>La Cantidad de clicks totales es de <b>Resta</b> {{ restar }}</p>
    <p>La Cantidad de clicks totales es de <b>Multiplicar</b> {{ multiplicar }}</p>
    <p>La Cantidad de clicks totales {{ sumar+restar+multiplicar }}</p>
    <p><a href="https://www.linkedin.com/in/brunomentasti/">Bruno Mentasti</a> - Cómision 23345 - Vue.js </p>
  </div>
</template>
<script>
export default {
  name: 'Contador',
  data() {
    return {
      contadorPadre: 0,
      sumar: 0,
      restar: 0,
      multiplicar: 0
    };
  },
  methods: {
    aumenta() {
      this.contadorPadre += 1;
      this.sumar++;
    },
    resta() {
      this.contadorPadre -= 1;
      this.restar++;
    },
    multi() {
      this.contadorPadre *= 2;
      this.multiplicar++;
    },
    reset() {
      this.contadorPadre = 0;
    }
  }
}
</script>
<style scoped>
h1 {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  font-size: 24px;
  text-transform: uppercase;
}
h2 {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  font-size: 34px;
  text-transform: uppercase;
}
p {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  font-size: 12px;
}
a {
  text-decoration: none;
  color:#2c3e50;
}
button {
  background-color: limegreen;
  border: none;
  color: white;
  padding: 10px 20px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
  margin: 4px 2px;
  cursor: pointer;
  -webkit-transition-duration: 0.4s;
  transition-duration: 0.4s;
}
button:hover {
  box-shadow: 0 12px 16px 0 rgba(0,0,0,0.24), 0 17px 50px 0 rgba(0,0,0,0.19);
}
</style>
