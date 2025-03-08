<script setup>

defineProps({
    friends:Array,
    userInfo:Object,
})
</script>
<template>
<h1>Complex Props</h1>
<h1>{{ friends }}</h1>
<h1>{{ userInfo }}</h1>
<hr />
<!-- !Iterating over Friends Array -->
<ul v-for="(friend, index) in friends" :key="index">
    <li>{{ friend }}</li>
</ul>

<!-- !Iterating over UserInfo Objects -->
<ul v-for="(Info, index) in userInfo" :key="index">
    <li>{{ Info }}</li>
</ul>
    


</template>