/! In reactive function we can't store primitive data types.

Creates a deeply reactive object (all nested properties are reactive).

Designed for complex state (objects, arrays, etc.).





<!-- !Does not work with primitives. -->
<!-- <script setup>
  import { reactive } from 'vue';
  let initialState = reactive(0)
  </script>
  <template>
<h1>Event Handler::{{ initialState }}</h1>
<button @click="initialState++">btn</button>
  </template> -->

<!-- !so we have to create reactive object. -->
<!-- <script setup>
  import { reactive } from 'vue';
  let initialState = reactive({ count: 0 })
  </script>
  <template>
<h1>Event Handler::{{ initialState.count }}</h1>
<button @click="initialState.count++">btn+</button>
<button @click="initialState.count--">btn-</button> 
  </template> -->
<!-- !!!!!! -->
<!-- <script setup>
import { reactive } from 'vue';
let initialState = reactive({
 val: {count: 0},
 user: ["Fahim","Reza"]})

const changeUser = () => {
    initialState.user[0] = "Shafin"
    initialState.user[1] = "Ahmed"
}
</script>
<template>
<h1>Current Count::{{ initialState.val.count }}</h1>
<h1>Users::{{ initialState.user }}</h1>

<button @click="initialState.val.count +=10">Add 10</button><br>

<button @click="initialState.val.count -=10">Reduce 10</button><br>

<button @click="changeUser">Change User</button><br>

<button @click="initialState.user.push('Fahim Reza')">Add One More</button>
</template> -->

<!-- ! -->
<!-- <script setup>
import { reactive } from 'vue';

let state = reactive({
 val: {count: 0},
 user: ["Fahim","Reza"]})

const changeUser = () => {
    state.user[0] = "Shafin"
    state.user[1] = "Ahmed"
} -->

//  Modify properties directly (no .value)
// state.user.name = 'Bob'; // Triggers reactivity
<!-- </script> -->

<!-- <template>
<h1>Users::{{ state.user }}</h1>
<button @click="changeUser">Change User</button><br>

<button @click="state.user.push('Fahim Reza')">Add One More</button>
<button @click="state.user.pop('')">reduce One More</button>
<button @click="state.user.unshift('')">UnShift</button>
<button @click="state.user.shift('')">Shift</button>
</template> -->





<!--! Avoid destructuring reactive objects (use toRefs to retain reactivity): -->

<!-- const { user } = toRefs(state); // Now user is a reactive ref -->