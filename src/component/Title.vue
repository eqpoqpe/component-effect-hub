<template>
  <div @selectstart="disableSelectText($event)">{{ title }}</div>
</template>

<script>
export default {
  name: 'Title',
  props: ['title'],
  methods: {
    disableSelectText(e) {
      e.preventDefault();
    },
  },
};
</script>
