<template lang="pug">
  section
    .content
      h2 Envie-nos uma mensagem
      .card
        input(
          v-model.trim="message.name"
          placeholder="Nome"
          required
        )
        input(
          v-model.trim="message.email"
          placeholder="E-mail" type="email"
          required
        )
        textarea(
          v-model.trim="message.text"
          placeholder="Mensagem"
          required
        )
      .text-right
        button(
          title="Enviar mensagem"
          type="submit"
          @click="send"
        ) Enviar mensagem
</template>

<script>
export default {
  data: () => ({
    message: {}
  }),
  methods: {
    send() {
      alert('Mensagem enviada')
    }
  }
}
</script>

<style lang="postcss" scoped>
section {
  background-color: #212529;
}
.content {
  h2 {
    color: #f8f9fa;
  }
}
input,
textarea {
  border: none;
  outline: none;
  margin: 0;
  padding: 0.5em 0;
  background: transparent;
  font: inherit;
  color: #f1f3f5;
  width: 100%;
  margin-bottom: 2em;
  border-bottom: 1px dotted #f1f3f5;
}
textarea {
  resize: vertical;
  height: 5em;
}
.text-right {
  text-align: right;
}
button {
  color: #adb5bd;
  background-color: #343a40;
  cursor: pointer;
  display: inline-block;
  line-height: 1.5;
  padding: 0.5em 0.75em;
  border: 1px dotted transparent;
  transition: all 300ms ease;
  &:focus {
    outline: none;
    border-color: #e9ecef;
  }
  &:hover {
    color: #e9ecef;
    background-color: #495057;
  }
  &:active {
    color: #adb5bd;
    background-color: #171a1d;
  }
}
</style>
