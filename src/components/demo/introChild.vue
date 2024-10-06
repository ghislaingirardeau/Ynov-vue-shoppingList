<template>
  <div>
    <h2>{{ props.name }}</h2>
    <div>
      <button @click="count1++">+</button>
      {{ count1 }}
      <button @click="count1--">-</button>
    </div>
    <div>
      <button @click="count2++">+</button>
      {{ count2 }}
      <button @click="count2--">-</button>
    </div>
    <div>
      <button @click="getTotalInParent">Sum</button>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const props = defineProps({
  name: String
})

const emit = defineEmits(['getTotal'])

const count1 = ref(0)
const count2 = ref(0)

const getTotalInParent = () => {
  emit('getTotal', count1.value + count2.value)
}
</script>

<style lang="scss" scoped></style>
