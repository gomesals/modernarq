<template lang="pug">
  #product
    project-header(:project="project")
    project-content(:project="project")
    project-gallery(:gallery="project.images.gallery")
    last-projects
</template>

<script>
import ProjectHeader from '~/components/ProjectHeader'
import ProjectContent from '~/components/ProjectContent'
import ProjectGallery from '~/components/ProjectGallery'
import LastProjects from '~/components/LastProjects'
export default {
  head: () => ({
    title: 'Projeto'
  }),
  components: {
    ProjectHeader,
    ProjectContent,
    ProjectGallery,
    LastProjects
  },
  data: () => ({
    project: {
      title: 'Projeto',
      images: {
        main: 'https://picsum.photos/1200/600?image=1081',
        gallery: [
          {
            p: 'https://picsum.photos/300/200?image=1081',
            o: 'https://picsum.photos/1200/600?image=1081'
          },
          {
            p: 'https://picsum.photos/300/200?image=1076',
            o: 'https://picsum.photos/1200/600?image=1076'
          },
          {
            p: 'https://picsum.photos/300/200?image=1075',
            o: 'https://picsum.photos/1200/600?image=1075'
          },
          {
            p: 'https://picsum.photos/300/200?image=1048',
            o: 'https://picsum.photos/1200/600?image=1048'
          },
          {
            p: 'https://picsum.photos/300/200?image=1031',
            o: 'https://picsum.photos/1200/600?image=1031'
          },
          {
            p: 'https://picsum.photos/300/200?image=1033',
            o: 'https://picsum.photos/1200/600?image=1033'
          }
        ]
      },
      date: '18/04/2018',
      category: 'Design de interiores',
      author: 'Arquiteto Sr.',
      content: [
        'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed mauris sapien, gravida quis accumsan ut, auctor non nunc. Nulla vitae justo at mauris tincidunt sagittis vitae nec tellus. Sed non porta velit. Aenean tristique eu velit nec scelerisque. Phasellus facilisis consectetur sem, id euismod velit venenatis a. Morbi mattis tristique ligula eget vulputate. Vivamus pharetra rhoncus rhoncus. Nam dapibus lobortis pulvinar. In efficitur lacus at magna fermentum, id tincidunt metus eleifend.',
        'Nam eu tempus justo, <strong>non</strong> hendrerit sapien. Proin purus elit, bibendum id mattis a, consectetur sit amet orci. Integer tristique in tortor eu pellentesque. Aliquam ultricies iaculis eros, sed hendrerit sapien euismod in. Sed posuere justo mollis dui pharetra, nec cursus elit euismod. Morbi placerat dolor leo. Vestibulum lacus nunc, congue ut orci eu, tempor convallis velit. Sed feugiat dapibus turpis sit amet ultricies. Quisque efficitur in orci non sagittis. Phasellus id neque ut turpis efficitur maximus. Ut nunc eros, aliquam id porta ut, viverra vitae sapien. Integer iaculis auctor volutpat. Maecenas leo nisl, accumsan in feugiat a, sodales ac elit.',
        'Cras ut lectus massa. Vestibulum eu lacus a orci lobortis pharetra. Sed finibus nisl purus. Integer nec nunc quis urna bibendum ultrices. Donec feugiat ex ac mi varius eleifend. Aenean urna tortor, blandit eu turpis quis, accumsan commodo mi. Aenean ultricies nisl lorem, non tincidunt risus porttitor id. Curabitur dictum ex ac metus mattis, condimentum cursus tellus vehicula. Maecenas non fermentum enim. Aliquam blandit ornare sagittis. Vestibulum condimentum, tellus et elementum faucibus, tortor justo feugiat dolor, sit amet eleifend magna turpis eu elit. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Curabitur id mollis orci. In sed neque lobortis, ultricies libero eget, euismod purus. Nullam fermentum tempor suscipit.',
        'Pellentesque tempus turpis sed ex placerat maximus. Pellentesque eu est non metus imperdiet gravida. Aenean at eros blandit, pellentesque quam at, molestie mauris. In in leo vel leo laoreet consequat. Suspendisse bibendum scelerisque egestas. Sed cursus mauris quis lorem rutrum, ut mattis orci pellentesque. Sed vel ante sodales massa finibus aliquam et vitae nisi.'
      ]
    }
  })
}
</script>

<style lang="postcss" scoped>
#product>>>section {
  .content {
    ul {
      list-style: none;
      display: flex;
      flex-wrap: wrap;
      padding-left: 0;
      li {
        margin-bottom: 1.5rem;
      }
    }
  }
}
</style>
