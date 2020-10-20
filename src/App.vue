<template>
  <v-phone>
    <v-chat-simulator :messages="messages" @all-chat-bubbles-completed="logNotification"/>
  </v-phone>
</template>

<script>
import Phone from '@/components/Phone'
import ChatSimulator from 'vue-chat-simulator';

export default {
  components: {
    'v-phone': Phone,
    'v-chat-simulator': ChatSimulator
  },
  data() {
    return {
      messages: [
        'Heey 👋🏽 ',
        'Nice to meet you !',
        'My name is vue-chat-simulator 😄',
        'With me are you able to simulate a chat 💬',
        'Just pass an array of strings and leave the rest to me 😉',
        'Lets have some fun together 🙌🏽',
      ]
    }
  },
  methods: {
    logNotification() {
      console.log('All chat bubbles are completed');
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
