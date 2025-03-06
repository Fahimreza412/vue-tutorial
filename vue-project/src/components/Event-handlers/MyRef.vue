 <script setup> 

 import {ref} from "vue"

// ?for numbers::
 let count = ref(0)

// ?for Strings::
 let userName = ref('')

// ?for Arrays::
 let userList = ref(['Fahim','Reza','Shafin','Ahmed'])

//  !for BIO
let bio = ref({
    name:"fahim",
    age:20,
    location:['Rajshahi'],
    sex:true
})
 </script>  

 <template>
 <h1>Count:: {{ count }}</h1>
<button @click="count++">Increment</button>
<button @click="count--">Decrement</button>  

<!-- !for userName -->
  <h1>Username:: {{ userName }}</h1>
<button @click="userName = 'Shafin'">Add user</button>  

<!-- !for userList -->
 <h1 >User List:: {{ userList }}</h1>
<button @click="userList.push('Physics')">Add More User</button> 
<button @click="userList.pop('Coding')">POPping</button>  

<!-- !for BIO -->
  <h1>BIO::: {{ bio.name }}</h1>
<h1>{{ bio.age }}</h1>
<h1>{{ bio.location }}</h1>
<h1>{{ bio.sex }}</h1>  

<!-- *change all points -->
    <button @click="bio.name = 'Shafin'">Change Name</button>
 <button @click="bio.age = '24'">Change Age</button>
 <button @click="bio.location = ['Dhaka']">Change location</button>
 <button @click="bio.sex = 'false'">Change sex</button> 

</template>  
    



<!-- !let mix things up use ref & reactive -->
  <!-- <script setup>
    import { reactive, ref } from "vue";

    let friends = reactive([ref('Reza'),ref('lalu'),ref('kalu')])

 </script>
 <template>
<h1>1. {{ friends[0] }}</h1>
<h1>2. {{ friends[1] }}</h1>
<h1>3. {{ friends[2] }}</h1>

<button @click="friends[0] = 'hi'">thums up</button>

<button @click="friends[1] = 'bye'">thums down</button>

<button @click="friends[2] = 'peak'">thums peak</button>
</template>  -->

