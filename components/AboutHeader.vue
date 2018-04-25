<template lang="pug">
  header(:style="`background-image: url(${image}&blur)`")
    h1 Sobre
</template>

<script>
export default {
  props: ['image']
}
</script>

<style lang="postcss" scoped>
header {
  width: 100%;
  height: 17rem;
  background-color: #000;
  text-align: center;
  background-position: center center;
  background-repeat: no-repeat;
  background-size: cover;
  h1 {
    color: #fff;
    text-align: center;
    padding-top: 3.2em;
    letter-spacing: 0.025em;
    text-shadow: 0 1px 3px rgba(0, 0, 0, 0.2);
    text-transform: uppercase;
  }
}
</style>
