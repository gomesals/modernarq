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
  padding: 3em 0;
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
}
ul {
  list-style: none;
  padding-left: 0;
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
  width: 100%;
  li {
    width: 30%;
    margin-bottom: 1.5em;
    h3 {
      margin-bottom: 1em;
      color: #343a40;
    }
    p {
      color: #495057;
    }
  }
}
@media screen and (max-width: 768px) {
  section {
    .content {
      width: 96%;
      ul {
        li {
          width: 100%;
        }
      }
    }
  }
}
</style>


