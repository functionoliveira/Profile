<template>
  <div class="contact-section">
    <h2>Contato</h2>
    <div class="col">
      <text-field label="Seu Nome" v-model="fullName" :id="hash()" />
    </div>
    <div class="col">
      <text-field label="Seu E-mail" v-model="email" :id="hash()" />
    </div>
    <div class="col">
      <text-field label="Assunto" v-model="subject" :id="hash()" />
    </div>
    <div class="col">
      <text-area-field label="Sua Mensagem" v-model="message" />
    </div>
    <div class="submit">
      <glass-button label="Enviar" />
    </div>
  </div>
</template>

<script>
import TextField from '~/components/form/TextField.vue'
import TextAreaField from '~/components/form/TextAreaField.vue'
import GlassButton from '~/components/buttons/GlassButton.vue'
export default {
  components: { TextField, TextAreaField, GlassButton },
  data () {
    return {
      fullName: '',
      email: '',
      subject: '',
      message: ''
    }
  },
  methods: {
    hash () {
      const keys = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'y', 'z']
      return Array.from({length: 16}, (v, k) => {
        const index = Math.ceil(Math.random() * 9)
        return keys[index]
      }).join('')
    }
  }
}
</script>

<style lang="scss">
.contact-section {
  .text-field {
    margin-bottom: 16px;
  }

  .submit {
    margin-top: 32px;
    text-align: right;
  }
}
</style>
