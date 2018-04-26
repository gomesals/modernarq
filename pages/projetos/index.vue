<template lang="pug">
  section
    .content
      h1 Projetos
      ul
        li(
          v-for="(item, index) in projects"
          :key="index"
        )
          nuxt-link(
            :to="{name: 'projetos-id', params: {id: index}}"
            :title="item.title"
          )
            .bg(:style="`background-image: url(${item.preview})`")
            .text-right
              span {{ item.title }}
</template>

<script>
export default {
  head: () => ({
    title: 'Projetos'
  }),
  data: () => ({
    projects: [
      {
        title: 'Projeto 1',
        preview: 'https://picsum.photos/350/200?image=1076',
        bg: 'https://picsum.photos/100/100?image=1076&blur'
      },
      {
        title: 'Projeto 2',
        preview: 'https://picsum.photos/350/200?image=1081',
        bg: 'https://picsum.photos/100/100?image=1081&blur'
      },
      {
        title: 'Projeto 3',
        preview: 'https://picsum.photos/350/200?image=1031',
        bg: 'https://picsum.photos/100/100?image=1031&blur'
      },
      {
        title: 'Projeto 4',
        preview: 'https://picsum.photos/350/200?image=1033',
        bg: 'https://picsum.photos/100/100?image=1033&blur'
      },
      {
        title: 'Projeto 5',
        preview: 'https://picsum.photos/350/200?image=1081',
        bg: 'https://picsum.photos/100/100?image=1081&blur'
      },
      {
        title: 'Projeto 6',
        preview: 'https://picsum.photos/350/200?image=1076',
        bg: 'https://picsum.photos/100/100?image=1076&blur'
      },
      {
        title: 'Projeto 7',
        preview: 'https://picsum.photos/350/200?image=1031',
        bg: 'https://picsum.photos/100/100?image=1031&blur'
      },
      {
        title: 'Projeto 8',
        preview: 'https://picsum.photos/350/200?image=1033',
        bg: 'https://picsum.photos/100/100?image=1033&blur'
      },
      {
        title: 'Projeto 9',
        preview: 'https://picsum.photos/350/200?image=1081',
        bg: 'https://picsum.photos/100/100?image=1031&blur'
      }
    ]
  })
}
</script>

<style lang="postcss" scoped>
.content {
  h1 {
    text-shadow: 0 1px 3px rgba(0, 0, 0, 0.3);
    color: #212529;
    text-transform: uppercase;
    letter-spacing: 0.05em;
    margin-bottom: 3rem;
  }
  ul {
    justify-content: space-between;
    list-style: none;
    display: flex;
    flex-wrap: wrap;
    padding-left: 0;
    li {
      width: 30%;
      margin-bottom: 1.5rem;
      box-shadow: 0 3px 11px -4px rgba(0, 0, 0, 0.2);
      transition: all 300ms ease;
      background-color: #fff;
      border-radius: 4px;
      &:hover {
        transform: translateY(-2px);
      }
      a {
        display: block;
        text-decoration: none;
      }
      .bg {
        width: 100%;
        height: 200px;
        background-color: #222;
        background-position: center center;
        background-repeat: no-repeat;
        background-size: cover;
        border-top-left-radius: 4px;
        border-top-right-radius: 4px;
      }
      .text-right {
        padding: 1em;
        text-align: right;
        color: #343a40;
        transition: color 300ms ease;
        &:hover {
          color: #212529;
        }
      }
    }
  }
}

@media screen and (max-width: 768px) {
  .content {
    ul {
      li {
        width: 45%;
      }
    }
  }
}
@media screen and (max-width: 425px) {
  .content {
    ul {
      li {
        width: 100%;
      }
    }
  }
}
</style>
