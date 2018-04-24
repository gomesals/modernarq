<template lang="pug">
  #contact
    contact-header(:map="contact.map")
    contact-info(:contact="contact")
    contact-form()
</template>

<script>
import ContactHeader from '~/components/ContactHeader'
import ContactInfo from '~/components/ContactInfo'
import ContactForm from '~/components/ContactForm'
export default {
  components: { ContactHeader, ContactInfo, ContactForm },
  data: () => ({
    contact: {
      info: {
        address: {
          street: 'Rua 1, 300',
          zip: '11111-111',
          city: 'Cidade',
          state: 'Estado',
          district: 'Bairro'
        },
        contact: {
          time: ['Seg. à Sex.: 09 às 17', 'Sáb: 10 às 14'],
          phone: '(11) 1111-1111',
          email: 'email@arq.com'
        }
      },
      map: {
        image:
          'https://maps.googleapis.com/maps/api/staticmap?center=São+Paulo,+SP&zoom=14&scale=false&size=640x300&maptype=roadmap&format=png&visual_refresh=true',
        link: 'https://www.google.com/maps/dir//São+Paulo,+SP/'
      }
    }
  })
}
</script>
