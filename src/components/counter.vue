<template>
  <h2>Compteur</h2>
  <button @click="count++">Count is: {{ count }}</button>
</template>

<script setup>
import { ref } from 'vue'

const count = ref(0)
</script>

<style lang="scss" scoped></style>
