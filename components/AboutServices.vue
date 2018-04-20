<template lang="pug">
  section
    .content
      h2 Serviços
      ul
        li(v-for="(item, index) in services" :key="index")
          h3 {{ item.title }}
          p {{ item.content }}
</template>

<script>
export default {
  props: ['services']
}
</script>

<style lang="postcss" scoped>
section {
  background: #fff;
}
.content {
  h2 {
    color: #212529;
  }
}
ul {
  li {
    h3 {
      margin-bottom: 1em;
      color: #343a40;
    }
    p {
      color: #495057;
    }
  }
}
</style>


