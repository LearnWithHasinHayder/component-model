<script setup>
import {computed} from 'vue'
const props = defineProps(['name', 'label'])
const emit = defineEmits(['update:name'])

const personName = computed({
    get() {
        return props.name
    },
    set(value) {
        emit('update:name', value)
    }
})
</script>
<template>
    <label for="name">SingleitemY {{ label }}</label>
    <!-- <input type="text" name="name" id="name" v-model="personName" > -->
    <input type="text" name="name" id="name" :value="name" @input="$emit('update:name',$event.target.value)" >
</template>
<style></style>