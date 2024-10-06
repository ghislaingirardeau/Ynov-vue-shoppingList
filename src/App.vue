<template>
  <div>
    <h1>Hello Vue JS</h1>

    <ShoppingList familyMember="Tom" />
    <ShoppingList familyMember="Paul" />
    <ShoppingList familyMember="Lea" />
  </div>
</template>

<script setup>
import ShoppingList from './components/7-ShoppingList.vue'
</script>

<style scoped></style>
