<template>
    <h1 class="text-red">Global Styling</h1>
    <p class="local">Trying Local Scope in this Component</p>

</template>

<!-- !Global Style.  -->
<!-- <style> -->
/* !For make it local only in globalStyle use Scoped*/
<style scoped>
.text-red{
    color: rgb(207, 118, 10);

}
</style>