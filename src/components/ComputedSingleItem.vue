<script setup>
defineProps(['modelValue', 'label'])
const emit  = defineEmits(['update:modelValue'])

const updateModelvalue = (value) => {
    emit('update:modelValue', value)
}
</script>
<template>
    <label for="name">{{ label }}</label>
    <input type="text" name="name" id="name" 
    :value="modelValue" 
    @input="updateModelvalue($event.target.value)">
</template>
<style></style>