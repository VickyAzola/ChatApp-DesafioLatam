<script>
import axios from 'axios'
import UserCard from './UserCard.vue';
import ChatComponent from './ChatComponent.vue';

export default {
  name: 'MessageApp',
  components: { UserCard, ChatComponent },
  data() {
    return {
      userProfileLeft: null,
      userProfileRight: null,
      messages: []
    }
  },
  async created() {
    try {
      const url = 'https://randomuser.me/api/?results=2'
      const { data } = await axios.get(url)
      this.userProfileLeft = data.results[0] 
      this.userProfileRight = data.results[1] 
    } catch (error) {
      console.error(error)
    }
  },
  methods: {
    sendMessage(texto, color, name) {
      this.messages.push({texto, color, name})
    }
  }
}
</script>

<template>
  <header>
    <h1>Chat Mazinger</h1>
  </header>
  <main>
    <UserCard 
      v-if="userProfileLeft"
      :userProfile="userProfileLeft"
      @send-message="sendMessage"
    />
    <ChatComponent :sendedMessages="messages" />
    <UserCard 
      v-if="userProfileRight"
      :userProfile="userProfileRight"
      @send-message="sendMessage"
    />
  </main>
</template>

<style scoped>
main {
  display: grid;
  grid-template-columns: 1fr 2fr 1fr;
  place-content: center;
  min-height: 80vh;
  column-gap: 1rem;
}
</style>
