<script setup>
//!Dynamic Binding::
const imageInfo ={
    src:"https://images.unsplash.com/photo-1738494610263-4e27d9d4e201?w=500&auto=format&fit=crop&q=60&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxmZWF0dXJlZC1waG90b3MtZmVlZHwzNnx8fGVufDB8fHx8fA%3D%3D",
    alt:"Just a random Text",
    width:400,
    height:400,
}
</script>
<template>
 
<!-- <img :="imageInfo"> -->
<img v-bind:="imageInfo">

</template>