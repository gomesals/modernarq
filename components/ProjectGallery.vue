<template lang="pug">
  .gallery
    ul
      li(
        v-for="(item, index) in project.images.gallery"
        :key="index"
        :style="`background-image: url(${item.p})`"
      )
</template>

<script>
// TODO: add image view
export default {
  props: ['project']
}
</script>

<style lang="postcss" scoped>
.gallery {
  width: 70%;
  margin: 0 auto;
  ul {
    list-style: none;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    padding-left: 0;
    li {
      width: 32%;
      margin: 6px 0.6%;
      height: 200px;
      background-position: center center;
      background-repeat: no-repeat;
      background-size: cover;
      transition: all 300ms ease;
      box-shadow: 0 3px 11px -4px rgba(0, 0, 0, 0.2);
      &:hover {
        transform: scale(1.1) translateY(-2px);
      }
      &.view {
        box-shadow: none;
        transform: none;
        position: fixed;
        top: 5%;
        left: 5%;
        width: 90%;
        height: 90%;
        background-size: contain;
      }
    }
  }
}
@media screen and (max-width: 768px) {
  .gallery {
    width: 96%;
  }
}
</style>
