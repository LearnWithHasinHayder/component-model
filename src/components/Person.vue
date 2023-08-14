<script setup>
import SingleItem from './SingleItem.vue';
// import ComputedSingleItem from './ComputedSingleItem.vue';
defineProps(['person'])
</script>
<template>
    <p class="my-5">
        <h2 class="text-xl">Child</h2>
        {{ person.name }} is {{ person.age }} years old and works as a {{ person.occupation }}.
    </p>
    <p>
        <form class="flex flex-col">
            <!-- <label for="name">Name</label>
            <input type="text" id="name" v-model="person.name"> -->
            <!-- <label for="age">Age</label>
            <input type="number" id="age" v-model="person.age"> -->
            <!-- <label for="occupation">Occupation</label>
            <input type="text" id="occupation" v-model="person.occupation"> -->

            <SingleItem v-model="person.name" label="Name"/>
            <SingleItem v-model="person.age" label="Age"/>
            <SingleItem v-model="person.occupation" label="occupation"/>
            <!-- <ComputedSingleItem v-model="person.occupation" label="Occupation"/> -->
        </form>
    </p>
</template>
<style></style>