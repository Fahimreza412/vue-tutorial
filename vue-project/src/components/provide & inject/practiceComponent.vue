<script setup>
import {inject} from 'vue'
const friendList = inject('friends')
const games = inject('games')
const moreGamesList = inject('moreGames')


</script>
<template>
    <h1>practiceComponent</h1>
    <h2>Injecting array</h2>
<ul v-for="(friend,index) in friendList" :key="index">
    <li>{{ friend }}</li>
</ul>

<hr>
<!-- !provide Object -->
<h1>Injecting Object</h1>

<ul v-for="(game,index) in games" :key="index">
    <li>{{ game }}</li>
</ul>
<!-- !provide Array of Object -->
<h1>Injecting Array of Object</h1>

<ul v-for="(moreGame,index) in moreGamesList" :key="index">
    <li>{{ moreGame }}</li>
</ul>

<!-- * array of object destructuring -->

<h1>destructuring Array of Object</h1>

<ul v-for="({id, tittle,genre,platform,releaseDate},index) in moreGamesList" :key="index">
    <li>{{ id }}</li>
    <li>{{ tittle }}</li>
    <li>{{ genre }}</li>
    <li>{{ platform }}</li>
    <li>{{ releaseDate }}</li>
</ul>


</template>