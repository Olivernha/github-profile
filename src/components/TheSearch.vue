<template>
  <div class="flex justify-between bg-[#20293A] px-6 py-3 rounded-lg h-16 mt-10">
    <img src="../assets/resources/Search.svg" alt="logo" class="w-5" />
    <input @keyup.enter="handleSearch" v-model="searchInput" type="text"
      class="ml-3 border-none text-white md:w-100 placeholder:font-normal focus:outline-none" placeholder="Username" />
  </div>
</template>
<script setup>
import { ref } from 'vue';
const searchInput = ref('');
const emit = defineEmits(['search']);
const handleSearch = () => {
  if (searchInput.value.trim() !== '') {
    emit('search', searchInput.value);
  }
};

</script>
