<script setup>
// !for nested

// defineProps(['studentName','studentAge','studentLocation'])

// !using provide& inject::: 
import {inject}  from 'vue'
const studentName = inject('studentName')
const studentAge = inject('studentAge')
const studentLocation = inject('studentLocation')
</script>
<template>
    <h1>studentComponent(children)</h1>
    <h1>{{ studentName }}</h1>
    <h1>{{ studentAge }}</h1>
    <h1>{{ studentLocation }}</h1>
</template>