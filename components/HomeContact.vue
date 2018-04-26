<template lang="pug">
  section
    .content
      .item
        h3 Nos escreva
        p 
          a(:href="`mailto:${contact.info.contact.email}`") {{ contact.info.contact.email }}
      .item
        h3 Nos ligue
        p {{ contact.info.contact.phone }}
      .item
        h3 Nos visite
        p {{ contact.info.address.street }}
          br
          | {{ contact.info.address.zip }}
          br
          | {{ contact.info.address.city }}, {{ contact.info.address.state }}
        .text-right
          a(
            target="_blank"
            title="Abrir mapa"
            :href="contact.map.link"
          ) Abrir mapa
</template>

<script>
export default {
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

<style lang="postcss" scoped>
section {
  background: #212529;
  color: #e9ecef;
}
.content {
  display: flex;
  flex-wrap: wrap;
  .item {
    width: 33%;
    justify-content: space-between;

    h3 {
      color: #f8f9fa;
      text-transform: uppercase;
      letter-spacing: 0.05em;
      font-weight: 500;
      margin-bottom: 1em;
    }
    p {
      font-size: 0.9em;
    }
    a {
      text-decoration: none;
      border: 1px solid rgba(255, 255, 255, 0.75);
      border-radius: 4px;
      padding: 0.35em 0.5em;
      color: rgba(255, 255, 255, 0.75);
      font-size: 14px;
      transition: all 300ms ease;
      margin-top: 1em;
      display: inline-block;
      &:hover {
        background-color: #fff;
        color: #343a40;
      }
    }
  }
}
@media screen and (max-width: 768px) {
  .content {
    .item {
      width: 48%;
      margin-right: 0;
      margin-bottom: 2rem;
    }
  }
}
@media screen and (max-width: 425px) {
  section {
    .content {
      .item {
        width: 100%;
        margin-bottom: 3rem;
      }
    }
  }
}
</style>

