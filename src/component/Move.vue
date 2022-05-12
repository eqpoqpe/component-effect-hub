<template>
  <div @click="toggle = !toggle">
    <div class="scl" :class="{ move: toggle }"></div>
    <div class="scl" :class="{ move: toggle }"></div>
    <div class="scl" :class="{ move: toggle }"></div>
  </div>
</template>

<script>
export default {
  name: 'Move',
  data() {
    return {
      toggle: true,
    };
  },
};
</script>

<style>
.scl {
  width: 70%;
  height: 300px;
  position: absolute;
  overflow: hidden;
}

.post {
  position: absolute;
}
.scl:nth-child(1) {
  background-color: orange;
  transition: all 1000ms;
}

.scl:nth-child(2) {
  background-color: green;
  transition: all 700ms;
}

.scl:nth-child(3) {
  background-color: pink;
  transition: all 500ms;
}

.move {
  width: 20px;
}
</style>
