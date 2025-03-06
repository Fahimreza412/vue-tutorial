 <!-- <script setup> -->
//  ! will show the output.
// const isTrue = true

// !wont show anything
// const isTrue = false
// const isFalse = false

// !!!!!!!!
// const isTrue =false
// const isFalse =false

<!-- </script>  -->
<!-- <template> -->
    <!-- <div>
        <h1 v-if="isTrue">This will show if isTrue is true.</h1>
    </div> -->

    <!--! for all cond -->
    <!-- <h1 v-if="isTrue">This will show if isTrue is true.</h1>
    <h1 v-else-if="isFalse">This will Show if isFalse is true.</h1>
    <h1 v-else>This wll show if neither isTrue nor isFalse is true.</h1> -->

<!-- </template> -->


<!-- !2.....v-show  -->
 <!-- <script setup>
 import {ref} from 'vue'
//  let isVisible =ref(true)
 let isVisible =ref(false)
</script> -->
<!-- <template> -->
<!-- v-show -->
<!-- <h1 v-show="isVisible">This will be shown or hidden based on the value of isVisible</h1>
<button>toggleVisibility</button> -->

<!-- *toggle it -->

<!-- <button @click="isVisible = !isVisible">toggleVisibility</button> -->
<!-- </template> -->


<!-- !practice-4-start -->
<!-- <script setup>
import { ref } from 'vue'
// let isUserloggedIn = ref(true)
let isUserloggedIn = ref(false)
let userName = 'HUXN'
let showdetails = ref(isUserloggedIn)
</script> -->
<!-- <template>
<div>
    <h1 v-if="isUserloggedIn">welcome, {{ userName }}</h1>
    <h2 v-else>Please log in to access this content.</h2>
</div>
     

     <div v-show="showDetails">
        <h3>You are now able to  modify your dashboard.</h3>

     </div>
</template> -->

<!-- !practice-4-end -->


<!-- !practice-5-START -->
<!-- <script setup> 
 import {ref} from 'vue'
 const isActive = ref(true)
 //  const isActive = ref(false)
 </script>
<template>
    <div v-if="isActive">
        <h1>My Blog Post</h1>
        <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Modi, repellendus? Dolore accusamus minima neque aperiam exercitationem nostrum consectetur, accusantium necessitatibus.</p>
    </div>
    <button @click="isActive =!isActive">Toggle</button>
</template> -->
<!-- !practice-5-END -->
<!-- !practice-6-START -->
 <!-- <script setup>
import { ref } from 'vue';
// let passWord = ref('mypersonalpassword')
// let passWord = ref('d')
let passWord = ref(0)

</script>
<template>
<h1 v-if="passWord.length>8">Strong passWord</h1>
<h1 v-else-if="passWord.length<8">Weak passWord</h1>
<h1 v-else>Please enter your passWord</h1>
</template> -->



<!-- !............ -->
<!-- <template>
    <h1>a</h1>
    </template>  -->

    <!-- Basic v-if Rendering -->
    <!-- <script>
    export default {
      data() {
        return {
          isLoggedIn: false,
          username: 'JohnDoe',
          userRole: 'user',
          items: [],
          isDetailVisible: true,
          isActive: true,
          isDisabled: false
        }
      },
      methods: {
        // Example of dynamic conditional rendering
        toggleVisibility() {
          this.isDetailVisible = !this.isDetailVisible;
        }
      },
      computed: {
        // Computed property for complex conditions
        shouldRenderSpecialContent() {
          return this.isLoggedIn && this.userRole === 'admin';
        }
      }
    }
    </script> -->
<!-- <template>
    <div> -->
      <!-- Simple v-if condition -->
      <!-- <div v-if="isLoggedIn">
        Welcome, {{ username }}!
      </div>
      <div v-else>
        Please log in
      </div> -->
  
      <!-- Multiple conditions with v-else-if -->
      <!-- <div v-if="userRole === 'admin'">
        Admin Dashboard
      </div>
      <div v-else-if="userRole === 'manager'">
        Manager Dashboard
      </div>
      <div v-else>
        User Dashboard
      </div> -->
  
      <!-- Rendering with template wrapper -->
      <!-- <template v-if="items.length > 0">
        <h2>Item List</h2>
        <ul>
          <li v-for="item in items" :key="item.id">
            {{ item.name }}
          </li>
        </ul>
      </template>
      <p v-else>No items available</p> -->
  
      <!-- v-show alternative -->
      <!-- <div v-show="isDetailVisible">
        Detailed Information
      </div> -->
  
      <!-- Conditional class binding -->
      <!-- <div 
        :class="{ 
          'active': isActive, 
          'disabled': isDisabled 
        }"
      >
        Conditionally Styled Element
      </div>
    </div>
  </template> -->
  
  
  
  <!-- <style scoped>
  .active {
    background-color: green;
    color: white;
  }
  .disabled {
    background-color: gray;
    opacity: 0.5;
  }
  </style> -->