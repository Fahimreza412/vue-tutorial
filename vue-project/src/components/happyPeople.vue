<!-- !js -->
<!-- <script>
console.log("hy");
</script> -->

<!-- !HTML -->
<!-- <template>
    <h1>Hey good people.how are you doing.</h1>
</template> -->

<!-- !CSS -->
 <!-- <style>
h1{
    color: rgb(241, 141, 10);
}
</style> -->


<!-- !for nested part -->

<script setup> 
import nestedCOm from './nesttedCOm.vue'
</script>

<template>
    <!-- !this is our parent part -->
    <h1>This is a parent component</h1>
    <!-- !calling our component(children-part) -->
<nestedCOm />
    
    </template>