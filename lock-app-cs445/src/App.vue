
<script setup>
import { ref } from 'vue'

import LoginPage from './components/loginPage.vue'
import HomePage from './components/homePage.vue'
//import LockDetails from './components/LockDetails.vue'

const page = ref('login')
</script>

<template>
  <div class="app">

    <LoginPage v-if= "page==='login'" @login="page ='home'"/>

    <HomePage v-if= "page==='home'"/>

  </div>
</template>