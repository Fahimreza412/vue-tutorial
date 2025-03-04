<script setup>
const myGithub = "https://github.com/"
const myImage = "https://images.unsplash.com/photo-1737917818689-f3b3708de5d7?q=80&w=1263&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D"
const altText = "Random picture"
const imageWidth = 400
const imageHeight = 500


</script>

<template>
    <!-- !Not this way:; -->
    <!-- <a href="https://github.com/"></a> -->
    <!-- !But this way:; -->
    <!-- <a  v-bind:href="myGithub">MY github link is here</a> -->
    <!-- ?Or this way -->
    <a  :href="myGithub">MY github link is here</a>

    <!-- !Adding height and width to the image. -->
    <img :src="myImage" :alt="altText" :width="imageWidth":height="imageHeight">
</template>