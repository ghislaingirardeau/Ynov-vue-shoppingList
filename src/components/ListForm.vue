<template>
  <form class="add-item-form" v-if="props.editing" @submit.prevent="formSumit">
    <input v-model.trim="newItemForProps.newItem" type="text" placeholder="Add an item" />
    <label>
      <input type="checkbox" v-model="newItemForProps.newItemHighPriority" />
      <strong>High Priority</strong>
    </label>
    <button :disabled="newItemForProps.newItem.length < 5" class="btn btn-primary">
      Save Item
    </button>
  </form>
</template>

<script setup>
const props = defineProps({
  editing: Boolean
})

const newItemForProps = defineModel()

const emit = defineEmits(['saveItem'])
function formSumit() {
  emit('saveItem')
}
</script>

<style lang="scss" scoped></style>
