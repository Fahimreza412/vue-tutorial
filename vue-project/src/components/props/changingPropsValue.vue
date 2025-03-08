<script setup>
// import {ref} from "vue"

const props = defineProps(['num'])


// !but this number is not changeable once it is fixed.. 
// props.num = 10


</script>
<template>

<h1>{{ props.num }}</h1>

</template>