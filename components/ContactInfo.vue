<template lang="pug">
  section
    .content
      h2 Entre em contato
      .info
        .address
          #city
            | {{ contact.info.address.city }}, {{ contact.info.address.state }}
          #street {{ contact.info.address.street }}
          #zip {{ contact.info.address.zip }}
          a(
            target="_blank"
            title="Visualizar no mapa"
            :href="contact.map.link"
          ) Visualizar no mapa
        .contact
          .time
            strong Horário de funcionamento
            #open(v-for="item in contact.info.contact.time") {{ item }}
          #phone {{ contact.info.contact.phone }}
          #email {{ contact.info.contact.email }}
</template>

<script>
export default {
  props: ['contact']
}
</script>

<style lang="postcss" scoped>
section {
  background-color: #fff;
  padding-bottom: 3rem;
}
.content {
  .info {
    display: flex;
    .address,
    .contact {
      padding: 2rem;
      flex-grow: 1;
    }
    .address {
      text-align: right;
      a {
        text-decoration: none;
        border: 1px solid #212529;
        border-radius: 4px;
        padding: 0.5em 0.75em;
        color: #212529;
        font-size: 14px;
        transition: all 300ms ease;
        display: inline-block;
        margin-top: 2rem;
        &:hover {
          background-color: #212529;
          color: #f8f9fa;
        }
      }
    }
    .contact {
      border-left: 2px solid #868e96;
      .time {
        margin-bottom: 2rem;
      }
    }
  }
}
@media screen and (max-width: 560px) {
  .info {
    flex-direction: column;
    .address {
      text-align: left !important;
    }
    .contact {
      border-left: none !important;
      border-top: 2px solid #868e96;
    }
  }
}
</style>
