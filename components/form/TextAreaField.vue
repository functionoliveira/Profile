<template>
  <div class="text-field" v-bind:class="{ active: active || text }">
    <label :for="id">{{ label }}</label>
    <textarea :id="id" rows="15" :name="label" type="text" v-model="value" @focusin="() => active=true" @focusout="() => active=false"></textarea>
  </div>
</template>

<script>
export default {
  model: {
    event: 'update',
    prop: 'text'
  },
  props: {
    label: String,
    text: String,
    id: String
  },
  data () {
    return {
      active: false
    }
  },
  computed: {
    value: {
      get () {
        return this.text
      },
      set (val) {
        this.$emit('update', val)
      }
    }
  }
}
</script>

<style lang="scss" scoped>
.text-field {
  background: transparent;
  padding: 8px 4px;
  border-radius: 2px;
  margin: 6px 0;
  border-bottom: 2px solid white;
  transition: 0.10s all ease-in-out;
  cursor: text;

  label {
    display: block;
    color: white;
    cursor: pointer;
  }

  textarea {
    width: 100%;
    background: none;
    border: none;
    outline: none;
    color: white;
    resize: vertical;
  }

  &.active {
    box-shadow: inset 0px 6px 50px -20px #231ed266;
    border-radius: 2px;
    border-color: rgba(240, 20, 165, 0.4) ;
  }
}
</style>
