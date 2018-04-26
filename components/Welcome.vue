<template lang="pug">
  .bg(:style="`background-image: url(${image})`")
    h1 Modernarq
</template>

<script>
export default {
  data: () => ({
    image: 'https://picsum.photos/850/600?image=1031'
  })
}
</script>


<style lang="postcss" scoped>
.bg {
  width: 100%;
  height: 30rem;
  background-position: center center;
  background-repeat: no-repeat;
  background-size: cover;
  position: relative;
  z-index: -1;
  h1 {
    position: absolute;
    top: 35%;
    left: 10%;
    font-weight: 400;
    text-transform: uppercase;
    border: 4px solid #e9ecef;
    padding: 0.75em 1.5em;
    border-top-width: 0;
    color: #e9ecef;
    letter-spacing: 0.05em;
    border-right-width: 0;
  }
}
</style>
