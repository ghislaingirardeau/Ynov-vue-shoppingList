<template>
  <li
    @click="togglePurchased(props.item)"
    class="static-class"
    :class="{
      strikeout: props.item.purchased,
      priority: props.item.highPriority
    }"
  >
    {{ props.item.label }}
  </li>
</template>

<script setup>
const togglePurchased = (item) => {
  item.purchased = !item.purchased
}

const props = defineProps({
  item: {
    type: Object,
    required: true
  }
})
</script>

<style lang="scss" scoped></style>
