# Vue-chat-simulator-demo

Demonstration app for the vue-chat-simulator package
<br /><br />

## Motivation

When I planned my personal website, I was looking for a way to create a more personal experience with the user.
So I thought it would be pretty cool to give the user the feeling to communicate directly with him through a kind of chat.
<br /><br />

## NPM Package

```bash
npm install vue-chat-simulator
```

## Usage

```vue
<template>
  <v-chat-simulator :messages="messages" @all-chat-bubbles-completed="logNotification"/>
</template>

<script>
import ChatSimulator from 'vue-chat-simulator';

export default {
  components: {
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
```

## Setup Demo App
```
npm install
```

## Run Demo App
```
npm run serve
```
