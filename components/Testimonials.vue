<template lang="pug">
  section
    .content
      h2 Depoimentos
      ul
        li(v-for="(item, index) in testimonials")
          p "{{ item.text }}"
          .name
            span - {{ item.name }}
</template>

<script>
export default {
  data: () => ({
    testimonials: [
      {
        name: 'Depoente 1',
        text:
          'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed mauris sapien, gravida quis accumsan ut, auctor non nunc. Nulla vitae justo at mauris tincidunt sagittis vitae nec tellus.'
      },
      {
        name: 'Depoente 2',
        text:
          'Sed non porta velit. Aenean tristique eu velit nec scelerisque. Phasellus facilisis consectetur sem, id euismod velit venenatis a. Morbi mattis tristique ligula eget vulputate. Vivamus pharetra rhoncus rhoncus. Nam dapibus lobortis pulvinar.'
      },
      {
        name: 'Depoente 3',
        text:
          'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed non porta velit. Aenean tristique eu velit nec scelerisque. Phasellus facilisis consectetur sem, id euismod velit venenatis a. Morbi mattis tristique ligula eget vulputate. Vivamus pharetra rhoncus rhoncus.'
      }
    ]
  })
}
</script>

<style lang="postcss" scoped>
section {
}
.content {
  ul {
    display: flex;
    li {
      width: 30%;
      margin-right: 1.5%;
      margin-left: 1.5%;
      transition: all 300ms ease;
      box-shadow: 0 3px 11px -4px rgba(0, 0, 0, 0.2);
      background-color: #fff;
      padding: 2rem;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      &:hover {
        transform: translateY(-2px);
      }
      p {
        margin-bottom: 1em;
        color: #495057;
      }
      .name {
        text-align: right;
        span {
          color: #adb5bd;
        }
      }
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
