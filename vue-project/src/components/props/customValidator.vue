<script setup>
defineProps({
    name:{
       type: String,
    validator: (propValue) =>  ['Fahim','Reza','web','developer'].includes(propValue)
    
    },

    age: {
        type: Number,
    validator: (propValue) => 
         (propValue >=  18 && propValue <= 30 ? true : false)
    }
    ,
    password: {
        type:String,
        validator: (propValue) => propValue.length >= 8 
    } 
})
</script>
<template>
    <h1>Custom validator</h1>
<h1>Name::{{ name }}</h1>
<h1>Age::{{ age }}</h1>
<h1>Password::{{ password }}</h1>

</template>