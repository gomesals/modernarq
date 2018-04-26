<template lang="pug">
  #home
    welcome
    about-services(:services="services")
    last-projects
    testimonials
    home-contact
</template>

<script>
import Welcome from '~/components/Welcome'
import AboutServices from '~/components/AboutServices'
import LastProjects from '~/components/LastProjects'
import Testimonials from '~/components/Testimonials'
import HomeContact from '~/components/HomeContact'
export default {
  components: {
    Welcome,
    AboutServices,
    LastProjects,
    Testimonials,
    HomeContact
  },
  data: () => ({
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
  })
}
</script>


<style lang="postcss" scoped>
#home>>>section {
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
