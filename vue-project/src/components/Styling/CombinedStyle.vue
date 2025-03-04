<template>
    <h2 class="g-1">Another GlobalStyle</h2>
    <h2 class="l-1">Another LocalStyle</h2>
</template>

<!-- !Global Styling -->
<style>
.g-1{
    background-color: cadetblue;
    color: coral;
}
</style>

<!-- !local Styling -->
<style scoped>
.l-1{
    background-color: rgb(150, 160, 95);
    color: rgb(255, 80, 80);
}
</style>