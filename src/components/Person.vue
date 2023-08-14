<script setup>
defineProps(['person'])
</script>
<template>
    <p class="my-5">
        <h2 class="text-xl">Child</h2>
        {{ person.name }} is {{ person.age }} years old and works as a {{ person.occupation }}.
    </p>
    <p>
    <form action="" class="flex flex-col">
        <label for="name">Name</label>
        <input type="text" name="name" id="name" v-model="person.name">
        <label for="age">Age</label>
        <input type="number" name="age" id="age" v-model="person.age">
        <label for="occupation">Occupation</label>
        <input type="text" name="occupation" id="occupation" v-model="person.occupation">
        <button class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded my-5 w-48">
            Update
        </button>
    </form>
    </p>
</template>
<style></style>