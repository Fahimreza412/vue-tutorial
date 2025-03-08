<script setup>
import { ref } from 'vue'
const username = ref('')
const email = ref('')
const password = ref('')

</script>
<template>
<h1>formComponent Event</h1>
<form @submit.prevent="$emit('userInfo',username,email,password)">
    <input type="text" placeholder="Enter Your Username" v-model="username"><br>
<input type="email" placeholder="Enter Your Email" v-model="email"><br>
<input type="password" placeholder="Enter Your password" v-model="password">

<button type="submit">Submit</button>

</form>

</template>