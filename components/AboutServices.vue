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
  list-style: none;
  padding-left: 0;
  display: flex;
  flex-wrap: wrap;
  width: 100%;
  li {
    margin-bottom: 1.5rem;
    width: 30%;
    margin-right: 3%;
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
      ul {
        justify-content: space-between;
        li {
          width: 48%;
          margin-right: 0;
        }
      }
    }
  }
}
@media screen and (max-width: 425px) {
  section {
    .content ul {
      li {
        width: 100%;
      }
    }
  }
}
</style>
