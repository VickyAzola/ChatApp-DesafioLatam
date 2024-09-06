<script>
export default {
  name: 'ChatComponent',
  props: ['sendedMessages'],
  methods: {
    isRightUser(userName) {
      return (
        this.$parent.userProfileRight.name.first === userName.first && 
        this.$parent.userProfileRight.name.last === userName.last
      );
    }
  }
}
</script>

<template>
  <section v-if="sendedMessages">
    <div 
      class="chatbox" 
      v-for="(message, index) in sendedMessages" 
      :key="index"
      :class="{ right: isRightUser(message.name) }"
    >
      <p class="nombre">{{ message.name.first }} {{ message.name.last }}</p>
      <p class="texto" :style="{backgroundColor: message.color}">{{ message.texto }}</p>
    </div>
  </section>
</template>

<style scoped>
section {
  background-color: rgb(217, 232, 236);
  padding: 1.5rem;
  border-radius: .5rem;
  overflow-y: scroll;
  max-height: 20.5rem;
}

.chatbox {
  margin-block: .2rem;
}

.chatbox.right {
  display: flex;
  flex-direction: column;
  align-items: end;
}

.nombre {
  color: rgb(134, 122, 122);
  font-size: .9rem;
  margin: 0;
}

.texto {
  margin-top: .2rem;
  margin-bottom: 0;
  padding: .2rem .5rem;
  border-radius: .5rem;
  max-width: max-content
}

</style>