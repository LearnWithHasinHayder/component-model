<script setup>
const props = defineProps(['name', 'label'])
const emit = defineEmits(['update:name'])

function reverseItem(){
    emit('update:name', props.name.split('').reverse().join(''))
}

</script>
<template>
    <h2 class="text-2xl">Button Item</h2>
    <!-- <label for="name">{{ name }}</label> -->
    <button @click="reverseItem()" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded"> Update {{label}}</button>
</template>
<style></style>