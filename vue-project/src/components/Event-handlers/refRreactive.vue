
<!-- !Exercise 1. Shopping Cart -->

Exercise 1.: Shopping Cart

Goal: Track items in a cart (reactive) and calculate the total price (computed ref).

Hint: Use reactive for cart items and ref for a computed total.

<!-- <script setup>
import { reactive, computed } from 'vue';

const cart = reactive([
  { name: 'Apple', price: 2 },
  { name: 'Banana', price: 1 },
]);

const total = computed(() => cart.reduce((sum, item) => sum + item.price, 0));
</script>

<template>
  <h3>Cart Total: ${{ total }}</h3>
  <ul>
    <li v-for="(item, index) in cart" :key="index">
      {{ item.name }} - ${{ item.price }}
    </li>
  </ul>
</template> -->

<!-- !Exercise 2. Dynamic Styling -->
Goal: Change a box’s color using a reactive object and adjust its size with a ref.

Hint: Use reactive for styles and ref for size.

Solution:

 <!-- <script setup>
import { reactive, ref } from 'vue';

const boxStyles = reactive({
  backgroundColor: 'lightblue',
  width: '100px',
  height: '100px',
});

const size = ref(100);

const increaseSize = () => {
  size.value += 10;
  boxStyles.width = `${size.value}px`;
  boxStyles.height = `${size.value}px`;
};
</script>

<template>
  <div :style="boxStyles"></div>
  <button @click="boxStyles.backgroundColor = 'lightgreen'">Green</button>
  <button @click="increaseSize">Grow</button>
</template>  -->


3. Challenge Exercise
<!-- !Exercise 3: Live Markdown Preview -->
Goal: Create a live Markdown previewer where:

Input text is stored in a ref.

Preview HTML is rendered using a reactive method.

<!-- <script setup>
import { ref, reactive } from 'vue';
// import marked from 'marked'; // Assume marked is installed

const markdownText = ref('# Hello World');
const preview = reactive({
  html: computed(() => marked(markdownText.value)),
});
</script>

<template>
  <div class="editor">
    <textarea v-model="markdownText"></textarea>
    <div v-html="preview.html" class="preview"></div>
  </div>
</template> -->

<!-- ! Real-Time Search Filter-->

4. Challenge: Real-Time Search Filter
Combine ref for search input and reactive for data:

<!-- <script setup>
import { reactive, ref, computed } from 'vue';

const products = reactive([
  { name: 'Laptop', price: 999 },
  { name: 'Phone', price: 699 },
  { name: 'Tablet', price: 299 },
  { name: 'Perfume', price: 399 }
]);

const searchQuery = ref('');

// Computed filtered list
const filteredProducts = computed(() => {
  return products.filter(product =>
    product.name.toLowerCase().includes(searchQuery.value.toLowerCase())
)});
</script>

<template>
  <input v-model="searchQuery" placeholder="Search..." />
  <ul>
    <li v-for="(product, index) in filteredProducts" :key="index">
      {{ product.name }} - ${{ product.price }}
    </li>
  </ul>
</template>  -->

<!-- !Dynamic Element Resizer -->

Example 5.: Dynamic Element Resizer
Resize a box using a reactive style object and a ref for DOM measurement:

<!-- <script setup>
import { reactive, ref, onMounted } from 'vue';
const boxRef = ref(null);
const boxStyle = reactive({
  width: '100px',
  height: '100px',
  backgroundColor: 'tomato'
});

const measureBox = () => {
  if (boxRef.value) {
    alert(`Width: ${boxRef.value.offsetWidth}px`);
  }
};
</script>

<template>
  <div ref="boxRef" :style="boxStyle"></div>
  <button @click="boxStyle.width = '200px'">Double Width</button>
  <button @click="measureBox">Measure</button>
</template> -->

<!-- !Advanced DOM Interaction -->

6. Advanced DOM Interaction
Example 7: Scroll Position Tracker
Use a template ref to track scroll position of a div:

<!-- <script setup>
import { ref, onMounted } from 'vue';
const scrollContainer = ref(null);
const scrollY = ref(0);

onMounted(() => {
  scrollContainer.value.addEventListener('scroll', () => {
    scrollY.value = scrollContainer.value.scrollTop;
  });
});
</script>

<template>
  <div ref="scrollContainer" style="height: 200px; overflow-y: scroll">
    <div style="height: 1000px">
      Scroll position: {{ scrollY }}px
    </div>
  </div>
</template> -->


<!-- ! Timer with Laps-->
Example 7: Timer with Laps
Track time with a ref and store lap times in a reactive array:
<!-- <script setup>
import { reactive, ref } from 'vue';
const timer = ref(0);
const laps = reactive([]);
let intervalId = null;

const startTimer = () => {
  intervalId = setInterval(() => timer.value++, 1000);
};
const addLap = () => {
  laps.push(timer.value);
};
</script>

<template>
  <button @click="startTimer">Start</button>
  <button @click="addLap">Add Lap</button>
  <p>Time: {{ timer }} seconds</p>
  <h4>Laps:</h4>
  <ul>
    <li v-for="(lap, index) in laps" :key="index">Lap {{ index + 1 }}: {{ lap }}s</li>
  </ul>
</template> -->

<!-- !Task Manager -->
Example 8.: Task Manager
Combine reactive for a task list and ref for new task input:

<!-- <script setup>
import { reactive, ref } from 'vue';
const tasks = reactive([]);
const newTask = ref('');

const addTask = () => {
  if (newTask.value.trim()) {
    tasks.push({ id: Date.now(), text: newTask.value });
    newTask.value = '';
  }
};
</script>

<template>
  <input v-model="newTask" placeholder="Add a task" />
  <button @click="addTask">Add</button>
  <ul>
    <li v-for="task in tasks" :key="task.id">{{ task.text }}</li>
  </ul>
</template> -->

<!-- !Color Picker-->

Example 9: Color Picker
Use a reactive object to control RGB color values:

<!-- <script setup>
import { reactive } from 'vue';
const color = reactive({ r: 0, g: 0, b: 0 });
</script>

<template>
  <input v-model="color.r" type="range" min="0" max="255" /> Red
  <input v-model="color.g" type="range" min="0" max="255" /> Green
  <input v-model="color.b" type="range" min="0" max="255" /> Blue
  <div 
    :style="{
      width: '100px',
      height: '100px',
      backgroundColor: `rgb(${color.r}, ${color.g}, ${color.b})`
    }"
  ></div>
</template> -->


<!-- !User Profile Editor -->
Example 10: User Profile Editor
Edit a user’s profile stored in a reactive object:

<!-- <script setup>
import { reactive } from 'vue';
const user = reactive({
  name: 'John',
  age: 30,
  email: 'john@example.com'
});
</script>

<template>
  <input v-model="user.name" placeholder="Name" />
  <input v-model="user.age" type="number" placeholder="Age" />
  <input v-model="user.email" placeholder="Email" />
  <div>
    <h3>Profile Preview:</h3>
    <p>Name: {{ user.name }}</p>
    <p>Age: {{ user.age }}</p>
    <p>Email: {{ user.email }}</p>
  </div>
</template> -->


<!-- ! Toggle Visibility-->
Example 11: Toggle Visibility
Show/hide content with a boolean ref:

<!-- <script setup>
import { ref } from 'vue';
const isVisible = ref(false);
</script>

<template>
  <button @click="isVisible = !isVisible">
    {{ isVisible ? 'Hide' : 'Show' }} Message
  </button>
  <p v-if="isVisible">Hello, Vue!</p>
</template> -->

<!-- ! Character Counter-->

Example 12.: Character Counter
<!-- Track the length of text in a <textarea> using a ref: -->

<!-- <script setup>
import { ref } from 'vue';
const text = ref('');

// Computed property for character count
const charCount = ref(0);
</script>

<template>
  <textarea v-model="text" @input="charCount = text.length"></textarea>
  <p>Characters: {{ charCount }}</p>
</template> -->
