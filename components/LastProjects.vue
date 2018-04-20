<template lang="pug">
  section(:style="projectBg")
    .content
      h2 Últimos projetos
      ul
        li(
          v-for="(item, index) in projects"
          :key="index"
          :style="`background-image: url(${item.preview})`"
        )
          nuxt-link(
            :to="{name: 'projeto-id', params: {id: 1}}"
            :title="item.title"
          )
            .title {{ item.title }}
</template>

<script>
export default {
  computed: {
    projectBg() {
      return `background-image: url(${this.projects[this.active].bg})`
    }
  },
  mounted() {
    setInterval(() => {
      this.nextBg()
    }, 10000)
  },
  methods: {
    nextBg() {
      if (this.active + 1 === this.projects.length) {
        this.active = 0
      } else {
        this.active++
      }
    }
  },
  data: () => ({
    active: 0,
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
      }
    ]
  })
}
</script>

<style lang="postcss" scoped>
section {
  background-color: #343a40;
  background-position: center center;
  background-repeat: no-repeat;
  background-size: cover;
  transition: background 300ms ease;
  .content {
    h2 {
      text-shadow: 0 1px 3px rgba(0, 0, 0, 0.3);
      color: #fff;
    }
    ul {
      justify-content: space-between;
      li {
        width: 49%;
        height: 200px;
        background-color: #222;
        background-position: center center;
        background-repeat: no-repeat;
        background-size: cover;
        box-shadow: 0 3px 11px -4px rgba(0, 0, 0, 0.2);
        transition: all 300ms ease;
        &:hover {
          transform: translateY(-2px);
        }
        a {
          display: block;
          width: 100%;
          height: 100%;
          text-decoration: none;
          position: relative;
          background: linear-gradient(transparent, rgba(0, 0, 0, 0.4) 90%);
          &:hover {
            .title {
              color: #f8f9fa;
            }
          }
          .title {
            position: absolute;
            bottom: 1em;
            right: 1em;
            font-size: 1.15em;
            color: #dee2e6;
            transition: color 300ms ease;
          }
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
