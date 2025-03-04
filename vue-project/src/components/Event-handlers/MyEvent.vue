<!-- !Reactivity won't work -->
<!-- <script setup>
  let count =0
  </script>
  <template>
<h1>Event Handler::{{ count }}</h1>
  </template> -->
<!--!using ref() or reactive()  statement  Reactivity  work -->
 <!-- <script setup>
import { ref } from "vue";
  let count = ref(0)
  let count1 = ref(0)

const incrementCounter = () => count1.value++ 
const decrementCounter = () => count1.value-- 

  </script>
  <template>
<h1>Event Handler::{{ count }}</h1> -->
<!-- !OR use v-on -->
 <!-- <button v-on:click="count++"> Increment</button><br> -->
<!-- !OR use @ -->
 <!-- <button @click="count--"> Decrement</button> -->


<!-- *For Arrow function -->
 <!-- <h1>Event Handler(For Arrow function)::{{ count1 }}</h1>  -->
<!-- !OR use v-on -->
 <!-- <button v-on:click="incrementCounter"> Increment2</button><br>  -->
<!-- !OR use @ -->
 <!-- <button @click="decrementCounter"> Decrement2</button>  
   </template>  -->

<!--! for form -->

   <!-- <script setup>
  const submitHandler = (e) => {
    e.preventDefault()
    alert('valid Credentials')
  }
  </script>
  <template>
<form @:submit="submitHandler">
<input type="text" placeholder="Please Enter Your Name">
<input type="email" placeholder="Please Enter Your email">
<button type="submit">Submit</button>

</form>
  </template>  -->


  <!-- !~111 -->

  <!-- <script setup>
  const showMessage = (message) => 
    alert(message)
  
  </script>
  <template>

<button @click="showMessage('This is my message')">Submit</button>
  </template> -->
  