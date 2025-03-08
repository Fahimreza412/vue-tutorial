<!-- !V-Model -->
 <!-- it is a directive that provides two-way data binding on an input, textarea or select element.It creates a connection between the data in your component and the input field ,allowing changes in one to automatically in one to automatically update the other and vice-versa -->

<script setup>

import {ref} from 'vue'
const formData = ref({username:"", email:"",   password:"" })

</script>

<template>
    <form>
<!-- !if we want to prevent this just use @submit.prevent -->

        <input type="text" placeholder="Please enter your name" v-model="formData.username" /><br>
        <input type="email" placeholder="Please enter your email" v-model="formData.email" /><br>
        <input type="password" placeholder="Please enter your password" v-model="formData.password" />
        <button type="submit">submit</button>
    </form>

 <h1>{{ formData.username}}</h1>
 <h1>{{ formData.email}}</h1>
 <h1>{{ formData.password}}</h1>
 
</template>