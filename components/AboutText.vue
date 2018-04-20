<template lang="pug">
  section
    .content
      h2 Sobre nós
      p(v-for="(item, index) in text") {{ item }}
</template>

<script>
export default {
  props: ['text']
}
</script>

<style lang="postcss" scoped>
section {
  padding: 1em 0;
}
.content {
  width: 70%;
  margin: 0 auto;
  h2 {
    margin-bottom: 1.5em;
    text-transform: uppercase;
    letter-spacing: 0.05em;
    color: #212529;
  }
  p {
    // max-width: 50em;
    font-size: 16px;
    line-height: 1.5;
    color: #343a40;
    margin: 0 auto 2em;
  }
}
</style>

