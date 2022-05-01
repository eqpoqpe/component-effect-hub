<template>
  <div class="wave"></div>
</template>

<script>
export default {
  name: 'Status',
};
</script>

<style scoped>
.wave {
  position: relative;
  /* align-items: center; */
  width: 100%;
  height: 337px;
  background-color: black;
}

.wave::before,
.wave::after {
  content: '';
  position: absolute;
  left: 50%;
  min-width: 300px;
  min-height: 300px;
  background-color: pink;
  animation-name: rotate;
  animation-iteration-count: infinite;
  animation-timing-function: linear;
}

.wave::before {
  bottom: 15px;
  border-radius: 43%;
  animation-duration: 10s;
}

.wave::after {
  background-color: red;
  bottom: 10px;
  opacity: 0;
  border-radius: 47%;
  animation-duration: 10s;
}

@keyframes rotate {
  0% {
    transform: translate(-50%, 0) rotateZ(0deg);
  }
  50% {
    transform: translate(-50%, -2%) rotateZ(180deg);
  }
  100% {
    transform: translate(-50%, 0%) rotateZ(360deg);
  }
}
</style>
