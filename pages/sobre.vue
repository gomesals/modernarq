<template lang="pug">
  #about
    about-header(:image="about.image")
    about-text(:text="about.text")
    about-services(:services="about.services")
    about-team(:team="about.team")
</template>

<script>
import AboutHeader from '~/components/AboutHeader'
import AboutServices from '~/components/AboutServices'
import AboutText from '~/components/AboutText'
import AboutTeam from '~/components/AboutTeam'
export default {
  head: () => ({
    title: 'Sobre'
  }),
  components: { AboutHeader, AboutServices, AboutText, AboutTeam },
  data: () => ({
    about: {
      team: [
        {
          name: 'Membro 1',
          image: 'https://picsum.photos/300/200?image=1005'
        },
        {
          name: 'Membro 2',
          image: 'https://picsum.photos/300/200?image=996'
        },
        {
          name: 'Membro 3',
          image: 'https://picsum.photos/300/200?image=1012'
        }
      ],
      image: 'https://picsum.photos/800/400?image=998',
      text: [
        'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus in ultrices eros. Cras quis hendrerit justo. Suspendisse commodo, turpis vitae dignissim tristique, dolor mi mattis nulla, non suscipit diam leo sit amet augue. Vestibulum vitae magna feugiat, varius libero sed, eleifend orci. Integer gravida tempus volutpat. Nullam at ipsum fringilla, dictum augue at, tincidunt diam. In hac habitasse platea dictumst. Integer posuere massa eu aliquam mollis. Curabitur congue est vitae turpis consequat, luctus fringilla lacus malesuada. Aliquam congue volutpat mollis. Vivamus vitae molestie diam. Quisque vitae augue vitae mauris molestie ornare vel at sapien. Morbi consectetur sem ac risus iaculis, at finibus magna consequat. Morbi elit erat, elementum non varius sed, pretium eu felis. Quisque a neque aliquam, bibendum est et, bibendum ligula.',
        'Cras accumsan neque luctus mauris egestas, quis aliquet turpis mattis. Maecenas mi nunc, lacinia et mi sit amet, tristique tincidunt mi. Donec at condimentum sapien, interdum laoreet lacus. Aenean aliquam ut nisi non elementum. Vestibulum luctus nisl at sapien vestibulum maximus. Integer viverra ipsum gravida ante tempus, vitae porta augue mattis. Integer condimentum molestie molestie. Pellentesque at ligula mollis, porta risus a, accumsan mi. Donec bibendum pellentesque ex, quis aliquet metus fermentum eu. In hac habitasse platea dictumst. Pellentesque hendrerit dolor a diam maximus, sed ornare urna interdum. Vivamus dictum magna in ex tristique dictum.',
        'Nam sollicitudin nulla quis nibh fringilla convallis. Etiam tincidunt erat arcu, at facilisis mi ultricies nec. Quisque ut nulla varius, tincidunt libero interdum, porttitor eros. Quisque vitae est ut orci dictum sagittis. In id rhoncus enim. Maecenas scelerisque et mauris quis posuere. Proin condimentum ipsum ex. Fusce porttitor lobortis libero, quis consectetur dolor ultrices eget. Integer pellentesque nibh a justo facilisis, ac dictum augue feugiat. Nulla vitae tincidunt quam. Aliquam ullamcorper scelerisque suscipit.'
      ],
      services: [
        {
          title: 'Arquitetura',
          content:
            'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut in felis pellentesque, bibendum neque non, fermentum ante. Sed ac turpis eu dui tempus rhoncus id vitae lacus. In hac habitasse platea dictumst. Donec pellentesque egestas leo. Phasellus nec euismod dui, in convallis nulla. Praesent vel sapien condimentum, pretium ipsum nec, eleifend quam. Donec tempor risus magna, non sagittis massa sed.'
        },
        {
          title: 'Design de Interiores',
          content:
            'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut in felis pellentesque, bibendum neque non, fermentum ante. Sed ac turpis eu dui tempus rhoncus id vitae lacus. In hac habitasse platea dictumst. Donec pellentesque egestas leo. Phasellus nec euismod dui, in convallis nulla. Praesent vel sapien condimentum, pretium ipsum nec, eleifend quam. Donec tempor risus magna, non sagittis massa sed.'
        },
        {
          title: 'Plantas',
          content:
            'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut in felis pellentesque, bibendum neque non, fermentum ante. Sed ac turpis eu dui tempus rhoncus id vitae lacus. In hac habitasse platea dictumst. Donec pellentesque egestas leo. Phasellus nec euismod dui, in convallis nulla. Praesent vel sapien condimentum, pretium ipsum nec, eleifend quam. Donec tempor risus magna, non sagittis massa sed.'
        }
      ]
    }
  })
}
</script>
