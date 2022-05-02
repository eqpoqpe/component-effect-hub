<template>
  <div class="wave-running" ref="wave"></div>
  <div class="wave-running-black" ref="wave"></div>
</template>

<script>
export default {
  name: 'Status',
  mounted() {},
};
</script>

<style scoped>
.wave-running {
  background: transparent;
  position: relative;
  align-items: center;
  width: 100%;
  height: 337px;
}

.wave-running::before,
.wave-running::after {
  background: linear-gradient(#e66465, #9198e5);
  content: '';
  position: absolute;
  left: 50%;
  min-width: 300px;
  min-height: 300px;
  animation-name: rotate-mix;
  animation-iteration-count: infinite;
  animation-timing-function: linear;
  animation-play-state: running;
}

.wave-running::before {
  bottom: 10px;
  opacity: 0.6;
  border-radius: 44%;
  animation-duration: 6s;
}

.wave-running::after {
  bottom: 13px;
  opacity: 0.6;
  border-radius: 47%;
  animation-duration: 10s;
}

.wave-running-black {
  background: transparent;
  position: relative;
  align-items: center;
  width: 100%;
  height: 337px;
}

.wave-running-black::before,
.wave-running-black::after {
  background-color: black;
  content: '';
  position: absolute;
  left: 50%;
  min-width: 300px;
  min-height: 300px;
  animation-name: rotate-mix;
  animation-iteration-count: infinite;
  animation-timing-function: linear;
  animation-play-state: running;
}

.wave-running-black::before {
  bottom: 10px;
  opacity: 0.6;
  border-radius: 44%;
  animation-duration: 6s;
}

.wave-running-black::after {
  bottom: 13px;
  opacity: 0.6;
  border-radius: 44%;
  animation-duration: 10s;
}

@keyframes rotate-mix {
  0% {
    transform: scale(1) translate(-50%, 0) rotateZ(0deg);
  }
  25% {
    transform: scale(0.95) translate(-52%, 0) rotateZ(90deg);
  }
  50% {
    transform: scale(0.9) translate(-55%, 0%) rotateZ(180deg);
  }
  75% {
    transform: scale(0.95) translate(-52%, 0) rotateZ(270deg);
  }
  100% {
    transform: scale(1) translate(-50%, 0%) rotateZ(360deg);
  }
}
</style>
