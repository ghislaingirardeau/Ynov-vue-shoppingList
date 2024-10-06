<template>
  <div>
    <IntroChild name="Compteur" @getTotal="getTotal" />
    <p>Voici le total {{ total }}</p>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import IntroChild from './introChild.vue'

const total = ref(0)

const getTotal = (payload) => {
  console.log(payload)
  total.value = payload
}
</script>

<style lang="scss" scoped></style>
