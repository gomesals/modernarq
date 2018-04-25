<template lang="pug">
  navbar(:class="{fluid, dark, transparent}")
    .nc
      .home
        nuxt-link(:to="{name: 'index'}" :title="name")
          img(v-if="hasImage" :src="image" :alt="name")
          span(v-else) {{ name }}
      .nav
        .toggle(
          @click="isMenuVisible = !isMenuVisible"
          :class="{menuTrigger: isMenuVisible}"
        )
          span
          span
          span
        ul(:class="{visible: isMenuVisible}")
          li(
            v-for="(item, index) in links"
            :key="index"
          )
            nuxt-link(:to="{name: item.link}") {{ item.text }}
</template>

<script>
export default {
  props: {
    image: {
      type: String,
      default: null
    },
    transparent: {
      type: Boolean,
      default: false
    },
    dark: {
      type: Boolean,
      default: false
    },
    fluid: {
      type: Boolean,
      default: false
    }
  },
  data: () => ({
    isMenuVisible: false,
    name: 'Modernarq',
    links: [
      {
        text: 'Projetos',
        link: 'projetos'
      },
      {
        text: 'Sobre',
        link: 'sobre'
      },
      {
        text: 'Contato',
        link: 'contato'
      }
    ]
  }),
  computed: {
    hasImage() {
      return !!this.image
    }
  }
}
</script>

<style lang="postcss" scoped>
navbar {
  .nc {
    display: flex;
    justify-content: space-between;
    margin: 0 auto;
    width: 70%;
    min-width: 700px;
    margin: 0 auto;
    .home,
    .nav ul li {
      a {
        text-decoration: none;
        display: inline-block;
        text-decoration: none;
        transition: color 300ms ease;
      }
    }
    .home {
      width: 150px;
      a {
        font-size: 1.5em;
        line-height: 1.5;
        letter-spacing: 0.0075em;
        padding: 0.5em 0;
        img {
          height: 50px;
        }
        span {
          padding-top: 0.4795em;
          padding-bottom: 0.4795em;
          display: inline-block;
        }
      }
    }
    .nav {
      align-self: center;
      .toggle {
        color: #ccc;
        display: none;
        cursor: pointer;
        span {
          display: block;
          width: 33px;
          height: 4px;
          margin-bottom: 5px;
          position: relative;
          border-radius: 3px;
          z-index: 1;
          transform-origin: 4px 0px;
          transition: transform 500ms cubic-bezier(0.77, 0.2, 0.05, 1),
            background 500ms cubic-bezier(0.77, 0.2, 0.05, 1),
            opacity 550ms ease;
          &:first-child {
            transform-origin: 0% 0%;
          }
          &:nth-last-child(2) {
            transform-origin: 0% 100%;
          }
        }
        &.menuTrigger {
          span {
            opacity: 1;
            &:nth-child(1) {
              transform: rotate(45deg) translate(2px, -4px);
            }
            &:nth-child(2) {
              opacity: 0;
            }
            &:nth-child(3) {
              transform: rotate(-45deg);
            }
          }
        }
      }
      ul {
        padding-left: 0;
        list-style: none;
        li {
          display: inline-block;
          a {
            padding-left: 1em;
            padding-top: 0.5em;
            padding-bottom: 0.5em;
            text-transform: uppercase;
            letter-spacing: 0.005em;
          }
        }
      }
    }
  }
}
navbar {
  &,
  .nav ul {
    background-color: #fff;
  }
  color: #212529;
  display: block;
  .nc {
    .home,
    .nav ul li {
      a {
        color: #adb5bd;
        &:hover {
          color: #212529;
        }
      }
    }
    .nav {
      .toggle {
        &:hover {
          span {
            background: #868e96;
          }
        }
        span {
          background: #adb5bd;
        }
        &.menuTrigger {
          &,
          &:hover {
            span {
              background: #212529;
            }
          }
        }
      }
    }
  }
  &.fluid {
    .nc {
      width: 90%;
    }
  }
  &.dark {
    &,
    .nav ul {
      background-color: #212529;
    }
    color: #e9ecef;
    .nc {
      .home,
      .nav ul li {
        a {
          color: #adb5bd;
          &:hover {
            color: #f8f9fa;
          }
        }
      }
      .nav {
        .toggle {
          &.menuTrigger {
            span {
              background: #f8f9fa;
            }
          }
        }
      }
    }
  }
  &.transparent {
    &,
    .nav ul {
      background-color: transparent;
    }
  }
}
@media screen and (max-width: 768px) {
  navbar {
    padding-left: 2rem;
    padding-right: 2rem;
    .nc {
      width: 100%;
      min-width: initial;
      .nav {
        .toggle {
          display: block;
        }
        ul {
          position: absolute;
          right: 2.5rem;
          top: 6rem;
          border-radius: 4px;
          padding: 1rem;
          opacity: 0;
          transition: opacity 500ms ease;
          box-shadow: 0 3px 11px -4px rgba(0, 0, 0, 0.2);
          &.visible {
            opacity: 1;
          }
          li {
            display: block;
            text-align: right;
          }
        }
      }
    }
  }
  navbar {
    &.transparent.dark {
      .nc {
        .nav {
          ul {
            background-color: #212529;
          }
        }
      }
    }
    &.transparent {
      .nc {
        .nav {
          ul {
            background-color: #fff;
          }
        }
      }
    }
    &.fluid {
      .nc {
        width: 100%;
      }
    }
  }
}
</style>
