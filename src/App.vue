<script setup>
import { Authenticator } from '@aws-amplify/ui-vue'
import '@aws-amplify/ui-vue/styles.css'
import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
  <div id="app">
    <authenticator>
      <template v-slot="{ user, signOut }">
        <h1>Hello {{ user.username }}!</h1>
        <button @click="signOut">Sign Out</button>
        <HelloWorld msg="Welcome to Your Vue.js App" />
      </template>
    </authenticator>
  </div>
</template>

<script>

export default {
  name: 'App',
  components: {
    HelloWorld
  }
}
</script>
