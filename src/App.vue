<template>
  <div id="app">
    <h1>Component Effect Hub</h1>
    <p>Copyright (c) 2022 <span class="profile">Vu Coolgifts</span></p>
    <Status />
  </div>
</template>

<script>
import App from './app.util';
import Status from './component/Status.vue';
import Glass from './component/Glass.vue';

export default {
  name: 'App',
  components: { Status },
  methods: {
    plusOne() {},
    Show(s) {
      console.log('DONE', s);
    },
  },
  mounted() {},
  ...App(),
};
</script>

<style>
hr.style-two {
  border: 0;
  height: 1px;
  background-image: linear-gradient(
    to right,
    rgba(0, 0, 0, 0),
    rgba(0, 0, 0, 0.75),
    rgba(0, 0, 0, 0)
  );
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#app p {
  display: -webkit-flexbox;
  color: black;
  font-style: italic;
  font-size: 15px;
}

.profile {
  background-color: black;
  color: white;
  padding: 0px 3px 0px 3px;
  opacity: 0.75;
}
</style>
