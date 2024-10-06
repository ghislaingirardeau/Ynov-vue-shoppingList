<script setup>
import { computed, onMounted, onUnmounted, onUpdated, ref, watch } from 'vue'
import ListCard from './ListCard.vue'
import ListForm from './ListForm.vue'

/* ----------------- DATAS --------------------- */

const header = ref('Shopping List for ')
const editing = ref(false)
const items = ref([
  {
    id: 1,
    label: '10 party hats',
    purchased: true,
    highPriority: false
  },
  {
    id: 2,
    label: '2 board games',
    purchased: true,
    highPriority: false
  },
  {
    id: 3,
    label: '20 cups',
    purchased: false,
    highPriority: true
  }
])
const newItem = ref('')
const newItemHighPriority = ref(false)

const newItemForProps = ref({
  newItem: '',
  newItemHighPriority: false
})

/* ----------------- PROPS --------------------- */

const props = defineProps({
  familyMember: String
})

/* ----------------- COMPUTED --------------------- */

const countItems = computed(() => {
  return 'You have ' + items.value.length + ' items'
})

/* ----------------- WATCH --------------------- */

watch(editing, (nextValue, prevValue) => {
  if (!nextValue) {
    items.value = []
  }
})

/* ----------------- METHODS --------------------- */

const saveItem = () => {
  items.value.push({
    id: items.value.length + 1,
    label: newItemForProps.value.newItem,
    highPriority: newItemForProps.value.newItemHighPriority
  })
  newItemForProps.value.newItem = ''
  newItemForProps.value.newItemHighPriority = ''
}
const doEdit = (e) => {
  editing.value = e
  newItemForProps.value.newItem = ''
  newItemForProps.value.newItemHighPriority = ''
}

/* ----------------- HOOK CYCLE DE VIE --------------------- */
onUpdated(() => {
  console.log('updates: a chaque changement dans le DOM')
})
onMounted(() => {
  console.log('mounted', items.value)
})
onUnmounted(() => {
  console.log('Le composant est detruit: disparait du DOM')
})
</script>

<template>
  <div class="header">
    <h1>{{ header }} {{ props.familyMember }}</h1>
    <button v-if="editing" class="btn" @click="doEdit(false)">Cancel</button>
    <button v-else class="btn btn-primary" @click="doEdit(true)">Add Item</button>
  </div>
  <ListForm v-model="newItemForProps" :editing @saveItem="saveItem" />
  <ul>
    <ListCard v-for="item in items" :key="item.id" :item="item" />
  </ul>
  <p v-if="!items.length">Nothing to see here</p>
  <p>{{ countItems }}</p>
</template>
