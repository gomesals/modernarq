<template lang="pug">
  section
    .content
      h2 Galeria
      ul
        li(
          v-for="(item, index) in gallery"
          :key="index"
          :style="`background-image: url(${item.p})`"
          :title="`Imagem ${index + 1}`"
        )
</template>

<script>
// TODO: add image view
export default {
  props: ['gallery']
}
</script>

<style lang="postcss" scoped>
section {
  background: #fff;
  .content {
    h2 {
      color: #212529;
    }
    ul {
      li {
        width: 30%;
        margin-right: 1.5%;
        margin-left: 1.5%;
        height: 200px;
        background-position: center center;
        background-repeat: no-repeat;
        background-size: cover;
        transition: all 300ms ease;
        box-shadow: 0 3px 11px -4px rgba(0, 0, 0, 0.2);
        &:hover {
          transform: scale(1.1) translateY(-2px);
        }
        /* &.view {
          box-shadow: none;
          transform: none;
          position: fixed;
          top: 5%;
          left: 5%;
          width: 90%;
          height: 90%;
          background-size: contain;
        } */
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
