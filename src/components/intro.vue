<template>
  <!-- TEXT INTERPOLATION -->
  <h2>Message: {{ msg }}</h2>
  <!-- ATTRIBUTE BINDING -->
  <div v-bind:id="dynamicId"></div>
  <div :id="dynamicId">
    <h3 :class="dynamicClass">Titre de couleur blue</h3>
    <!-- Dans les moustaches, c'est du JS qui est interprété par le navigateur -->
    <!-- Mais attention à limité les fonctions à l'intérieur -->
    <h3 :class="dynamicClass">Titre de couleur {{ dynamicClass.toUpperCase() }}</h3>
  </div>
</template>

<script setup>
import { ref } from 'vue'

// TOUT CE QUI EST ECRIT ICI EST DU JS ET SERA LU PAR LE NAVIGATEUR
for (let index = 0; index < 3; index++) {
  console.log(index)
}

const msg = ref("On va décourvir Vue JS aujourd'hui")
const dynamicId = ref('12')
const dynamicClass = ref('blue')
</script>

<style lang="scss" scoped></style>
