<template lang="pug">
  section
    .content
      .info
        .item
          strong Arquiteto
          span {{ project.author }}
        .item
          strong Data
          span {{ project.date }}
        .item
          strong Categoria
          span {{ project.category }} 
      .text
        p(v-for="(item, index) in project.content" :key="index" v-html="item")
</template>

<script>
export default {
  props: ['project']
}
</script>

<style lang="postcss" scoped>
section{
  margin-top: -19rem;
}
.content {
  background: rgba(255, 255, 255, 0.6);
  border-radius: 4px;
  box-shadow: 0 3px 11px -4px rgba(0, 0, 0, 0.2);
  .info {
    display: flex;
    justify-content: space-around;
    background: rgba(255, 255, 255, 0.5);
    padding: 0.75rem 1.5rem;
    .item {
      color: #868e96;
      overflow: hidden;
      white-space: nowrap;
      text-overflow: ellipsis;
      strong {
        margin-right: 0.5em;
        font-weight: 500;
        color: #212529;
      }
    }
  }
  .text {
    padding: 1.5rem 1.5rem 1px;
    p {
      font-size: 16px;
      line-height: 1.5;
      color: #495057;
      margin-bottom: 1.5rem;
    }
  }
}
@media screen and (max-width: 768px) {
  .content {
    width: 96%;
    .info {
      flex-direction: column;
      .item {
        margin-bottom: 0.5em;
      }
    }
  }
}
</style>
