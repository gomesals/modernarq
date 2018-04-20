<template lang="pug">
  div
    nuxt
</template>

<style lang="postcss">
html {
  font-family: 'Open Sans', 'Segoe UI', Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*,
*:before,
*:after {
  box-sizing: border-box;
  margin: 0;
}

body {
  background-color: #f1f3f5;
}

section {
  padding: 3rem 0 1.5rem;
  .content {
    width: 70%;
    min-width: 700px;
    margin: 0 auto;
    h2 {
      margin-bottom: 1.5rem;
      text-transform: uppercase;
      letter-spacing: 0.05em;
    }
  }
}
@media screen and (max-width: 768px) {
  section {
    padding-left: 2rem;
    padding-right: 2rem;
    .content {
      width: 100%;
      min-width: initial;
    }
  }
}
</style>
