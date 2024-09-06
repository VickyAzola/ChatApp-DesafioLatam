<script>
export default {
  name: 'UserCard',
  props: ['userProfile'],
  emits: ['send-message'],
  data() {
    return {
      color: '',
      texto: '',
    }
  },
  methods: {
    sendMessage() {
      this.$emit('send-message', this.texto, this.color, this.userProfile.name)

      //limpiar texto
      this.texto = ''
    }
  }
}
</script>

<template>
  <section>
    <div>
      <img :src="userProfile.picture.large" :alt="userProfile.name.last" />
      <p>{{ userProfile.name.first }} {{ userProfile.name.last }}</p>
    </div>
    <form @submit.prevent="sendMessage">
      <input v-model="color" type="color" />
      <textarea v-model="texto"></textarea>
      <button>Enviar</button>
    </form>
  </section>
</template>

<style scoped>
div {
  text-align: center;
  margin-bottom: 1rem;
}

form {
  display: flex;
  flex-direction: column;
  row-gap: .3rem
}

input {
  width: 100%;
}

textarea {
  height: 7rem;
}

button {
  padding-block: .5rem;
}
</style>