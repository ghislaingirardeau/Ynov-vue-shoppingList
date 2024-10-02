<template>
  <div>
    <p>Message is: {{ message }}</p>
    <input v-model="message" placeholder="edit me" />
    <input type="checkbox" id="checkbox" v-model="checked" />
    <label for="checkbox">{{ checked }}</label>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const message = ref('old message')
const checked = ref(false)
</script>

<style lang="scss" scoped></style>
