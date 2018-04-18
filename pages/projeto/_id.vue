<template lang="pug">
  div
    project-header(:project="project")
    .content
      .info
        .item
          strong Arquiteto
          span Nome
        .item
          strong Data
          span Data
        .item
          strong Categoria
          span Categoria
      .text
        p lorem
        p lorem
        p lorem
        p lorem
</template>

<script>
import ProjectHeader from '~/components/ProjectHeader'
export default {
  components: { ProjectHeader },
  data: () => ({
    project: {
      title: 'Projeto',
      images: {
        main: 'https://picsum.photos/1200/600?image=1081'
      }
    }
  })
}
</script>

