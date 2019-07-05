<template>
  <div class="angles"/>
</template>

<script>
export default {
  name: 'background'
}
</script>

<style scoped>
.angles {
  background: linear-gradient(
    45deg,
    rgba(0, 79, 161, 0) 0%,
    rgba(0, 79, 161, 0.5) 45%,
    rgba(0, 79, 161, 0.75) 80%,
    rgba(0, 79, 161, 1) 100%
  );
  height: 1000px;
  z-index: -1;
  position: absolute;
  top: 72px;
}
</style>