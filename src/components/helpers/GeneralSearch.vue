<template>
  <div class="p-4 bg-white rounded-2xl shadow-md w-full max-w-md">
    <h2 class="text-xl font-bold mb-4">Find Your Adventure</h2>

    <div class="mb-4">
      <label class="block text-sm font-semibold mb-1">Destination</label>
      <select v-model="filters.destination" class="w-full border rounded p-2">
        <option value="">-- Select Destination --</option>
        <option v-for="dest in destinations" :key="dest" :value="dest">{{ dest }}</option>
      </select>
    </div>

    <div class="mb-4">
      <label class="block text-sm font-semibold mb-1">Adventure Type</label>
      <select v-model="filters.adventureType" class="w-full border rounded p-2">
        <option value="">-- Select Adventure --</option>
        <option v-for="type in adventureTypes" :key="type" :value="type">{{ type }}</option>
      </select>
    </div>

    <button @click="search" class="bg-orange-600 hover:bg-orange-700 text-white font-bold py-2 px-4 rounded w-full">
      Search Packages
    </button>
  </div>
</template>

<script setup>
import { reactive } from 'vue'

const filters = reactive({
  destination: '',
  adventureType: ''
})

const destinations = ['Nairobi', 'Masai Mara', 'Mombasa', 'Tsavo', 'Mount Kenya']
const adventureTypes = ['Safari', 'Beach Holiday', 'Hiking', 'Balloon Ride', 'Cultural Tour']

const emit = defineEmits(['search'])

function search() {
  emit('search', { ...filters })
}
</script>

<style scoped>
select {
  appearance: none;
}
</style>
