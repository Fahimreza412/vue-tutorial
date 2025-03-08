<!-- ?V-FOR -->
 The v-for directive is used to iterate over an array or an object and render a template for each item in the collection.
<!-- !WHY-::KEY -->
 <!-- *Efficient DOM Updates -->
  1.When vue renders a list of elements.It uses virtual Dom to determine the most efficienr way to update the actual DOM. The key helps vue identify which elements have changed,been added or been removed.
  2. Without keys,vue may need to recreate the entire DOM structure for each update,which can be less efficient.
<!-- !Avoiding Common pitfalls  -->
 1.Using key can help avoid common pitfalls,such as duplicate key warnings in the console or incorrect rendering when items are rearranged in the list.
 2.Vue relies on keys to track the identity of elementsand unique keys for each item ensures that vue can accurately update the dom based on changes in the list.



<!-- <script setup>
import {ref} from 'vue'
let people = ref(['fahim','Reza',"seii"])

</script>

<template>
    <h1 v-for="(person, index) in people" :key="index">{{ person }}</h1>
    <h1 v-for="(person, index) in people" :key="index">{{ index }}</h1>
</template> -->

<!-- !for object part -->

 <script setup>
import { ref } from 'vue'
const books = ref([
    {
        id:1,
        tittle:'To kill a mocking bird',
        author:"harper lee",
        genre:"Fiction",
        publicationYear:1960
    },
    {
        id:2,
        tittle:'1984',
        author:"George orwell",
        genre:"Dystopian",
        publicationYear:1969
    },
    {
        id:3,
        tittle:'The great getsby',
        author:"F.Scott fitzgerald",
        genre:"Classic",
        publicationYear:1925
    },
    {
        id:4,
        tittle:'The Catcher in the Rye',
        author:"J.D salinger",
        genre:"Coming-of-age",
        publicationYear:1960
    },
    {
        id:5,
        tittle:"Harry potter and the sorcerer  Stone",
        author:"harper lee",
        genre:"Fantasy",
        publicationYear:1997
    }
])

</script> 
 <template>
    <h3 v-for="(content,index) in books" :key="index">{{ content }}</h3> 
<!-- ?Now,destructring the object -->
 <ul v-for="({id,tittle,author,genre,publicationYear},i) in books" :key="i">
    <li>ID:: {{ id }}</li>
    <li>:: {{ tittle }}</li>
    <li>author:: {{ author }}</li>
    <li>genre:: {{ genre }}</li>
    <li>publicationYear:: {{ publicationYear }}</li>

</ul>
</template> 

<!-- !Example::2 -->
 <!-- <script setup>
 import {ref} from 'vue'
 const movies = ref([
    [
        'The Showshank Redemption',
        'The GodFather',
        'The Dark Knight',
        "Schindr's List",
        "The Green Mile"
    ],
    ["Pulp Fiction","Fight Club","Forest Gump","The silence of Lambs","The usual Suspects"],
    [
        "Inception",
        "The Matrix",
        "Interstellar",
        "Blonde Runner",
        "Eternal sunshine of the spotless Mind"
    ],
    ["The Lord Of The Rings","Star Mars","harry Potter","The Habbit","Jurrasic park"],
    ["Titanic","Avatar","The terminator","The Sixth Sense","Gladiator"]
 ])
</script> -->
<!-- <template> -->
    <!-- <ul v-for="(movie,i) in movies" :key="i"> -->
        <!-- <li>{{  movie  }}</li> -->
<!-- ?for nested loop -->
 <!-- <li v-for="(m,ind) in movie" :key="ind">{{ m }}</li>

    </ul>
</template> -->

<!-- !Example::3 -->

<!-- Example 8 -->
<!-- <script setup>
import { ref } from 'vue'
const complexGamesObj = ref({
  game1: {
    title: 'Space Explorer',
    genre: 'Sci-Fi',
    platform: 'PC',
    releaseDate: '2023-05-20'
  },
  game2: {
    title: 'Fantasy Quest',
    genre: 'Fantasy',
    platform: 'PlayStation',
    releaseDate: '2023-07-10'
  },
  movie1: {
    title: 'Inception',
    director: 'Christopher Nolan',
    genre: 'Sci-Fi',
    releaseDate: '2010-07-16'
  },
  movie2: {
    title: 'The Shawshank Redemption',
    director: 'Frank Darabont',
    genre: 'Drama',
    releaseDate: '1994-09-23'
  },
  book1: {
    title: 'Dune',
    author: 'Frank Herbert',
    genre: 'Science Fiction',
    publicationYear: 1965
  },
  book2: {
    title: 'To Kill a Mockingbird',
    author: 'Harper Lee',
    genre: 'Fiction',
    publicationYear: 1960
  }
})
</script>

<template>
  <ul v-for="({ title, author, genre, publicationYear }, index) in complexGamesObj" :key="index">
    <li>{{ title }}</li>
    <li>{{ author }}</li>
    <li>{{ genre }}</li>
    <li>{{ publicationYear }}</li>
  </ul>
</template> -->
<!-- ------------------------- -->

<!-- ------------------------- -->
<!--! Example::4 -->

<!-- <script setup>
import { ref } from 'vue'
const complexGamesObj = ref({
  game1: {
    title: 'Space Explorer',
    genre: 'Sci-Fi',
    platform: 'PC',
    releaseDate: '2023-05-20'
  },
  game2: {
    title: 'Fantasy Quest',
    genre: 'Fantasy',
    platform: 'PlayStation',
    releaseDate: '2023-07-10'
  },
  movie1: {
    title: 'Inception',
    director: 'Christopher Nolan',
    genre: 'Sci-Fi',
    releaseDate: '2010-07-16'
  },
  movie2: {
    title: 'The Shawshank Redemption',
    director: 'Frank Darabont',
    genre: 'Drama',
    releaseDate: '1994-09-23'
  },
  book1: {
    title: 'Dune',
    author: 'Frank Herbert',
    genre: 'Science Fiction',
    publicationYear: 1965
  },
  book2: {
    title: 'To Kill a Mockingbird',
    author: 'Harper Lee',
    genre: 'Fiction',
    publicationYear: 1960
  }
})
</script>

<template>
  <ul v-for="({ title, author, genre, publicationYear }, index) in complexGamesObj" :key="index">
    <li>{{ title }}</li>
    <li>{{ author }}</li>
    <li>{{ genre }}</li>
    <li>{{ publicationYear }}</li>
  </ul>
</template> -->
<!-- ------------------------- -->

<!-- ------------------------- -->
<!--! Example 5 -->


   <!-- <script setup>
import { ref } from 'vue'
const games = ref({
  id: 1,
  title: 'Epic Adventure Game',
  genre: ['Action', 'Adventure', 'RPG'],
  platform: ['PC', 'PlayStation', 'Xbox', 'Nintendo Switch'],
  releaseDate: '2022-03-15',
  developer: {
    name: 'Awesome Game Studios',
    location: 'San Francisco, CA',
    teamSize: 50
  },
  ratings: {
    metacritic: 90,
    user: 4.8
  },
  features: {
    singlePlayer: true,
    multiplayer: true,
    onlineCoop: true,
    splitScreen: false
  },
  systemRequirements: {
    minimum: {
      os: 'Windows 10',
      processor: 'Intel Core i5',
      memory: '8 GB RAM',
      graphics: 'NVIDIA GTX 970',
      storage: '50 GB available space'
    },
    recommended: {
      os: 'Windows 11',
      processor: 'Intel Core i7',
      memory: '16 GB RAM',
      graphics: 'NVIDIA RTX 3080',
      storage: '100 GB available space'
    }
  },
  storyline: 'Embark on a thrilling adventure to save the world from impending doom!',
  characters: ['Hero', 'Sidekick', 'Villain', 'NPCs'],
  achievements: [
    { id: 1, name: 'Master Explorer', description: 'Explore every corner of the game world' },
    { id: 2, name: 'Legendary Warrior', description: 'Complete the game on the hardest difficulty' }
  ]
})
</script> -->

<!-- <template>
  <ul v-for="(value, keys, index) in games" :key="value">
    {{
      index
    }}.
    {{
      keys
    }}
    👉
    {{
      value
    }}
  </ul>
</template>  -->

<!-- !Example::6 -->

 <!-- <script setup>
import { ref } from 'vue'
const complexGamesObj = ref({
  game1: {
    title: 'Space Explorer',
    genre: 'Sci-Fi',
    platform: 'PC',
    releaseDate: '2023-05-20'
  },
  game2: {
    title: 'Fantasy Quest',
    genre: 'Fantasy',
    platform: 'PlayStation',
    releaseDate: '2023-07-10'
  },
  movie1: {
    title: 'Inception',
    director: 'Christopher Nolan',
    genre: 'Sci-Fi',
    releaseDate: '2010-07-16'
  },
  movie2: {
    title: 'The Shawshank Redemption',
    director: 'Frank Darabont',
    genre: 'Drama',
    releaseDate: '1994-09-23'
  },
  book1: {
    title: 'Dune',
    author: 'Frank Herbert',
    genre: 'Science Fiction',
    publicationYear: 1965
  },
  book2: {
    title: 'To Kill a Mockingbird',
    author: 'Harper Lee',
    genre: 'Fiction',
    publicationYear: 1960
  }
})
</script>

<template> -->
<!-- ?Getting all objects -->
 <!-- <ul v-for="(game,ind) in complexGamesObj" :key="ind"> -->
    <!-- <li>{{ game }}</li> -->

    <!-- <br/> -->
    <!-- !Getting a single value from object -->
     <!-- <li v-for="(property,i) in game" :key="i">{{ property }}</li> -->
 <!-- </ul> -->


 <!-- ?Destructuring all objects -->
  <!-- <ul v-for="({ title, author, genre, publicationYear }, index) in complexGamesObj" :key="index">
    <li>{{ title }}</li>
    <li>{{ author }}</li>
    <li>{{ genre }}</li>
    <li>{{ publicationYear }}</li>
  </ul>
</template>  -->


<!-- !!! -->
 <!-- <script setup>

</script>
<template>
    <ul v-for="number in 10" :key="number">
        <li>{{ number }}</li>
    </ul>
</template> -->