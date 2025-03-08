<script setup>


</script>
<template>
<h1>Component Event</h1>

<button @click="$emit('incrementCounter')">+</button>
<button @click="$emit('decrementCounter')">+</button>
<!-- <button @click="decrementCounter">-</button> -->

</template>