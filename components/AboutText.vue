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
.content {
  h2 {
    color: #212529;
  }
  p {
    font-size: 16px;
    line-height: 1.5;
    color: #343a40;
    margin: 0 auto 1.5rem;
  }
}
</style>

