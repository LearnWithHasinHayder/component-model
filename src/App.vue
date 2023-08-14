<script setup>
import {reactive} from 'vue'
const person = reactive({
  name: 'John Doe',
  age: 30,
  occupation: 'Web Developer'
})

import Person from './components/Person.vue';
import SingleItem from './components/SingleItem.vue';
import SingleItemX from './components/SingleItemX.vue';
</script>

<template>
<section class="mx-auto container">
  <h1 class="my-10">Component Model</h1>
  <p class="my-5">
    <h2 class="text-xl">Parent</h2>
    {{ person.name }} is {{ person.age }} years old and works as a {{ person.occupation }}.
  </p>
  <Person :person="person" />
  <!-- <SingleItem :name="person.name" /> -->
  <SingleItem v-model="person.name"  />
  <SingleItemX v-model:name="person.name"  />
</section>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
