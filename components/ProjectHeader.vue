<template lang="pug">
  header(:style="`background-image: url(${project.images.main}&blur)`")
    h1 {{ project.title }}
</template>

<script>
export default {
  props: ['project']
}
</script>

<style lang='postcss' scoped >
header {
  height: 30rem;
  width: 100%;
  text-align: center;
  background-position: center center;
  background-repeat: no-repeat;
  background-size: cover;
  h1 {
    color: #fff;
    text-align: center;
    padding-top: 3em;
    letter-spacing: 0.025em;
    text-shadow: 0 1px 3px rgba(0, 0, 0, 0.2);
    text-transform: uppercase;
  }
}
</style>
