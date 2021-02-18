<template>
  <div class="contact-section">
    <h2>Contato</h2>
    <div class="row">
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
      <div class="col">
        <glass-button label="Enviar" />
      </div>
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

<style lang="scss" scoped>
</style>
