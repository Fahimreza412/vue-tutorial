<!-- !Computed properties -->
It is a special kind of variable that automatically updates itself whenever the data it depends on changes.
It's like a little worker that watches certain data,performs some work on it.and always gives you the most up to date result.

<!-- <script setup>
import {ref, computed } from 'vue' 
const num = ref(5)
const suqaredNum =computed(() => {
    return num.value * num.value
})

const firstName = ref('Fahim')
const lastName = ref('Reza')
const fullName = computed(() => firstName.value + ' ' + lastName.value)
</script>
<template>
    <h1>Original Number:: {{ num }}</h1>
    <h1>Squared Number:: {{ suqaredNum }}</h1>

    <h1>Full Name::{{ fullName }}</h1>


</template> -->

<!-- !Squarerd Number -->

<!-- <script setup>
import {ref,computed} from 'vue';
const counter = ref(0)
const suqaredNum = computed(() => counter.value ** 2)
const incrementCounter = () => {
    counter.value++
}
</script>
<template>
    <h1>Counter:: {{ counter }}</h1>
    <p>Squared Counter:: {{ suqaredNum }}</p>
    <button @click="incrementCounter">
        Increment Counter
    </button>
</template> -->

    <!-- !Cubic Number -->

    <script setup>
import { ref,computed  } from "vue";
const counter = ref(0)
const cubicNUm = computed(() => counter.value ** 3)
const incrementCounter = () => {
    counter.value++
}
const decrementCounter = () => {
    counter.value--
}
</script>
<template>
    <h1>Counter::{{ counter }}</h1>
    <p>Cubic Number:: {{ cubicNUm }}</p>
    <button @click="incrementCounter">Increment Counter</button>
    <button @click="decrementCounter">decrementCounter Counter</button>
</template>