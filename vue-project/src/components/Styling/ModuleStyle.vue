<template>
    <!-- <h1 v-bind:class="$style['.m-class']">Using Module Syntax with $ syntax (kebab-case)</h1> -->
    <!-- !for camelCase -->
<!-- <h1 :class="$style['m-class']">Using Module Syntax with $ syntax (kebab-case)</h1> -->


<!-- !for literal -->
<h1 :class="myClasses.anotherClass">Using Module Syntax with $ syntax (Camel-case)</h1>

</template>

<!-- <style module> -->
<style module ="myClasses">
/* !kebab Case */
.m-class{
    background-color: #e60808;
    color:beige ;
}

.anotherClass{
    background-color: #247504;
    color: antiquewhite;
}


</style>