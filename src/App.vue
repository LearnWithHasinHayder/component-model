<script setup>
import {ref, reactive} from 'vue'
import Person from './components/Person.vue'
import SingleItem from './components/SingleItem.vue'
import SingleItemY from './components/SingleItemY.vue'
import MultipleItem from './components/MultipleItem.vue'
import ButtonItem from './components/ButtonItem.vue'
const person = reactive({
  name: 'John Doe',
  age: 30,
  occupation: 'Web Developer',
})

// const name = ref("Jane Doe")

</script>

<template>
<section class="mx-auto container">
  <h1 class="my-10">Component Model</h1>
  <p class="my-5">
    <h2 class="text-xl">Parent</h2>
    {{ person.name }} is {{ person.age }} years old and works as a {{ person.occupation }}. {{ person.email }}
  </p>

  <Person :person="person"/>
  <!-- <SingleItem v-model="person.name" label="Name"/> -->

  <MultipleItem v-model:name="person.name" v-model:age="person.age" v-model:occupation="person.occupation"/>
  
  <!-- <hr/> -->

  <!-- <SingleItemY v-model:name="person.name" label="Name"/> -->

  <hr>

  <ButtonItem v-model:name="person.name" label="Name"/>
  <ButtonItem v-model:name="person.age" label="Age"/>
  <ButtonItem v-model:name="person.occupation" label="Occupation"/>
  <ButtonItem v-model:name="person.email" label="Email"/>

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
