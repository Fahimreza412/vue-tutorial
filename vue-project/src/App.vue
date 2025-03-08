<script setup>
// import happyPeople  from "./components/happyPeople.vue";

//!! text-interpolation
// import textInterpo from "./components/textInterpo.vue"

// !attribute binding::
// import attribute from "./components/Binding/attribute"

//!! Dynamic binding::
// import Dynamic from "./components/Binding/Dynamic"
// !Styling in depth::
// ?for global style

// import GlobalStyle from "./components/Styling/GlobalStyle.vue"
// ?for local style

// import LocalStyle from "./components/Styling/LocalStyle.vue"
// ?for Combined style
 
// import CombinedStyle from "./components/Styling/CombinedStyle.vue"
// ?for Moduled style

// import ModuleStyle from "./components/Styling/ModuleStyle.vue"

// !Event handler in vue.
//  import MyEvent from "./components/Event-handlers/MyEvent.vue"

// !!Reactive  function in vue
// import MyReactive from "./components/Event-handlers/MyReactive.vue"

// !!Ref  function in vue

// import MyRef from "./components/Event-handlers/MyRef.vue"

// ref & reactive combined both 
// import refReactive from "./components/Event-handlers/refRreactive.vue"

// !Computed properties

// import computed from "./components/Event-handlers/computed.vue"

// ! Job tracker::
// import JobTracker from "./components/Event-handlers/jobTracker.vue";
// import computed from "./components/Event-handlers/jobTracker.vue"

// !conditional Rendering
// import conditionalRendering from './components/conditional-Rendering/conditionalRendering.vue';

// !v-for:::

// import vFor from './components/vFor.vue';

// !v-MOdel:::

// import vModel from './components/vModel.vue';

// !Props:::

// import StaticPropsComponents from "./components/props/StaticPropsComponents.vue"

// !Dynamic-props
//  import {ref} from 'vue'
// const firstName = ref("Fahim")
// const lastName = ref("reza")

// import DynamicProps from "./components/props/DynamicProps.vue"

// !Changing-props
// import {ref} from 'vue'

// import changingPropsvalue from "./components/props/changingPropsValue.vue"
// const num = ref(69)


// !propValidation:::
// import {ref}  from 'vue'
// import propValidation from "./components/props/propValidation.vue"

// !ComplexProps::v

// import {ref} from 'vue'

// import ComplexProps from "./components/props/ComplexProps.vue"

// !ComplexProps::v
// import { ref } from 'vue'

//  import customValidator from "./components/props/customValidator.vue"

// !ComponentEvent(emit)
// import componentEvent from "./components/componentEvent/componentEvent.vue"
// import { ref } from 'vue'
// let count = ref(0)

// !Form component:::
// import formComponent from "./components/componentEvent/formComponent.vue"


// const formHandler = (username, email, password) => {
//    console.log('username', username);
//    console.log('email', email);
//    console.log('password', password);
   
// }

// !!!!!!Slot component::
// import { ref } from 'vue'

// import slotComponent from "./components/slots/slotComponent.vue"
// !!!!!!fallbackComponent Slot component::

// import { ref } from 'vue'

// import namedSlots from "./components/slots/namedSlots.vue"

// !defaultslot:::

// import { ref } from 'vue'

// import defaultSlot from "./components/slots/defaultSlots.vue"

// !Provide & inject:::
//  !StudentComponent

// import { ref } from 'vue'



// import studentComponent from "./components/provide & inject/studentComponent.vue"

// !School component

// !Typical way to call nested components..

//  import { ref } from 'vue'
//  import  schoolComponent from "./components/provide & inject/SchoolComponent.vue"

//  const studentName = 'Alex'
// const studentAge = 20
// const studentLocation = ['Rajshahi','Boalia']

// !!!!!!!!!!Using nested methods:::
//  import  schoolComponent from "./components/provide & inject/SchoolComponent.vue"
// import { provide } from 'vue'
// provide('studentName', 'Fahim' )
// provide('studentAge', 20 )
// provide('studentLocation', ['Rajshahi' ,'Boalia'] )

// !practiceComponent:::

// import { ref } from 'vue'
// import practiceComponent from './components/provide & inject/practiceComponent.vue'
// import {provide} from 'vue'

// !Provide Array
// provide('friends', ['shafin','ahmed','Fahim' ,'Reza'] )
// !provide Object:::
// provide('games', {
//    id:1,
//    tittle: 'Epic game Adventure',
//    genre:['action','Adventure','RPG' ],
//    Platform:['PC', 'PlayStation','XBox','Nintendo Switch' ],
//    releaseDate:['action','Adventure','RPG' ],
//    developer:{
//       name:'awesome Game Studios',
//       location:'San Fransisco,LA',
//       teamSize:50,
//    }}
// )

// !Provides Array of Objects:;

// provide('moreGames', [
//    {
//       id:2,
//       tittle: 'Space Explorer',
//       genre:'Sci-Fi',
//       platform:'PC',
//       releaseDate:'2023-05-20'
//    },
//    {
//       id:3,
//       tittle: 'Fantasy Quest',
//       genre:'Fantasy',
//       platform:'PlayStation',
//       releaseDate:'2023-07-20'
//    },
//    {
//       id:4,
//       tittle: 'Inception',
//       director:'Christopher Nolan',
//       genre:'Sci-Fi',
//       // platform:'PC',
//       releaseDate:'2023-05-20'
//    },
//    {
//       id:5,
//       tittle: 'The ShawsShank RedempTion',
//       director:'Frank Darabont',
//       genre:'Drama',
//       // platform:'PC',
//       releaseDate:'2023-05-20'
//    }
  
// ])


// !!LifeCycle component:::





</script>
<template>

<!-- <happyPeople /> -->
<!-- !text-interpolation -->
<!-- <textInterpo /> -->
 
<!-- *Binding Start -->
 <!-- !attribute -->
 <!-- <attribute/> -->
 <!-- !Dynamic -->
 <!-- <Dynamic/> -->
 <!-- *Binding Start -->


<!-- *Styling in vue(start) -->
<!-- !Styling in depth -->(GlobalStyle) 
<!-- <GlobalStyle/> -->
<!-- !Styling in depth -->(LocalStyle) 
<!-- <LocalStyle/> -->
<!-- !Styling in depth -->(CombinedStyle) 
<!-- <CombinedStyle/> -->
<!-- !Styling in depth --> (ModuledStyle) 
<!-- <ModuleStyle /> -->
<!-- *Styling in vue(End) -->

<!-- *Even handler in vue -->
<!-- !MyEvent -->
 <!-- <MyEvent/> -->
<!-- !MyReactive -->
<!-- <MyReactive/> -->

<!-- !MyRef -->

<!-- <MyRef/> -->

<!-- !ref & reactive both -->
 <!-- <refReactive/> -->
  <!-- !computed properties -->
   <!-- <computed/> -->

   <!-- !conditional rendering -->
   <!-- <conditionalRendering /> -->

<!-- !v-for -->
<!-- <vFor/>  -->

 <!-- !v-model -->

  <!-- <vModel/> -->


  <!-- ?props -->
   <!-- *Static Props -->

   <!-- <StaticPropsComponents name="fahim" age="23"/> -->

   <!-- *Dynamic props -->
   
   <!-- <DynamicProps  :firstName="firstName" :lastName="lastName" /> -->

   <!-- *Changing Props -->
    <!-- <changingPropsvalue :num="num" /> -->

    <!-- *PropValidation -->
     <!-- <propValidation :fullName="reza" :age="20"/> -->

<!-- !COmpelxProps -->

 <!-- <ComplexProps
  :friends="['alex','fahim','reza','ahmed']" 
 :userInfo="{ name:'alex', age:20, location: ['Rajshahi','IDK']} "/> -->

<!-- !customValidator -->
 <!-- <customValidator name="Reza" :age="20" password="randomPassword" /> -->

<!-- !componentEvent -->
 <!-- <h1>Count:: {{ count }}</h1>
 <componentEvent @incrementCounter="count++" @decrementCounter="count--"  /> -->

<!-- !formComponent -->

<!-- <formComponent @userInfo="formHandler" /> -->

<!-- !Slot -->
 <!--?not this way  -->
<!-- <slotComponent/> -->
 <!-- ?this way -->
  <!-- <slotComponent>
   <h1>Content1</h1>
  </slotComponent> -->
<!-- !fallbackContent -->

<!-- <hr/> -->
<!-- <fallcackContent></fallcackContent> -->
<!-- <fallcackContent>Fallback will not work because I'm providing content inside the component.</fallcackContent> -->

<!-- !NamedSlots -->
<!-- <namedSlots> -->

   <!-- ! v-slot:one -->
   <!-- <template v-slot:one>
      <h1>This content will go to slot "one"</h1>
   </template> -->

   <!--! #two -->
   <!-- <template #two>
      <h1>This content will go to slot "two"</h1>
   </template> -->

<!-- </namedSlots> -->

<!-- ?defaultSlots -->
 
<!-- <defaultSlot>
   <template #default>
      <h1>This is some random default content here</h1>

   </template>
</defaultSlot> -->

<!-- !!!!!Provide & Inject(start) -->
<!-- *student -->
<!-- <studentComponent/> -->

<!-- *School -->
<!-- ??typical way to call nested data -->
<!-- <schoolComponent :studentName="studentName" :studentAge="studentAge" :studentLocation="studentLocation" /> -->

<!-- *using provide & inject method::: -->

<!-- <schoolComponent/> -->

<!-- ?practice Component -->
 <practiceComponent/>


<!-- !!!!!Provide & Inject(End) -->
   <!-- !jobTracker -->
<!-- <JobTracker/> -->


</template>
<style scoped></style>