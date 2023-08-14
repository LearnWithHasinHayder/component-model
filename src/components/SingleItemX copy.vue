<script setup>
import {computed} from 'vue'
const props = defineProps(['name'])
const emit = defineEmits(['update:name'])

const personName = computed({
    get(){
        return props.name
    },
    set(value){
        emit('update:name', value)
    }
})
</script>
<template>
    <p class="my-5">
        <h2 class="text-xl">Single Item X</h2>
        name is {{ personName }} 
    </p>
    <p>
    <form action="" class="flex flex-col">
        <label for="name">Name</label>
        <input type="text" name="name" id="name" v-model="personName">
    </form>
    </p>
</template>
<style></style>