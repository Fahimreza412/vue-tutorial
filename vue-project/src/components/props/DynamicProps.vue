<script setup>
// import {ref} from "vue"

const props = defineProps(['firstName','lastName'])




</script>
<template>

<h1>{{ props.firstName }}</h1>
<h1>{{ props.lastName }}</h1>

</template>