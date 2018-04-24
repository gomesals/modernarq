<template lang="pug">
  header(:style="`background-image: linear-gradient(rgba(0, 0, 0, 0.75), rgba(0, 0, 0, 0.75) 50%), url(${map.image})`")
    h1 Contato
    a(
      target="_blank"
      title="Abrir mapa"
      :href="map.link"
    ) Abrir mapa
</template>

<script>
export default {
  props: ['map']
}
</script>

<style lang="postcss" scoped>
header {
  text-align: center;
  width: 100%;
  height: 40vh;
  background-color: #000;
  text-align: center;
  background-position: center center;
  background-repeat: no-repeat;
  background-size: cover;
  h1 {
    color: #f8f9fa;
    text-align: center;
    padding-top: 3.2em;
    letter-spacing: 0.025em;
    text-shadow: 0 1px 3px rgba(0, 0, 0, 0.2);
    text-transform: uppercase;
    margin-bottom: 1rem;
  }
  a {
    text-decoration: none;
    border: 1px solid rgba(255, 255, 255, 0.75);
    border-radius: 4px;
    padding: 0.35em 0.5em;
    color: rgba(255, 255, 255, 0.75);
    font-size: 14px;
    transition: all 300ms ease;
    &:hover {
      background-color: #fff;
      color: #343a40;
    }
  }
}
</style>
