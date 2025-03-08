<script setup>

import studentComponent from './studentComponent.vue'
// !for nested 
// defineProps(['studentName','studentAge','studentLocation'])

</script>
<template>
    // <h1>SchoolComponent</h1>
    <!-- ?for nested -->
    <!-- <studentComponent  :studentName="studentName" :studentAge="studentAge" :studentLocation="studentLocation" /> -->

<!-- !using provide & inject method::; -->
<studentComponent/>


</template>