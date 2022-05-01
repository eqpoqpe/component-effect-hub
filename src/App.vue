<script>
import AppUtil from './App.util';

export default {
  name: 'App',
  components: {},
  methods: {
    plusOne() {},
  },
  mounted() {},
  ...AppUtil(),
};
</script>

<template>
  <div id="app">
    <h1>Component Effect Hub</h1>
    <p>Copyright (c) 2022 <span class="profile">Vu Coolgifts</span></p>
  </div>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

#app p {
  color: black;
  font-style: italic;
  font-size: 15px;
}

.profile {
  background-color: black;
  color: white;
}
</style>
