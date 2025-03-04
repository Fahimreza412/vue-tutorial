<script setup>
// import textinterpo from './textInterpo.vue'
const msg = "Blue world"
const myNum = "01615653386"
function sum(x,y) {
    return x+y
}
</script>

<template>
    <h1>All about text Interpolation.</h1>
    <h1>{{ msg }}</h1>
    <h1>{{ myNum }}</h1>
    <h3>2*2</h3>
    <h1>  {{ 2 * 2 }}</h1>
    <p>Add two Numbers::::{{ sum(2,9) }}</p>
<!-- !not applicable -->
     <!-- <p>{{ const myName = "Reza" }}</p> -->
</template>

