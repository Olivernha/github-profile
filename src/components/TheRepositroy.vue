<template>
  <div v-for="r in repo"
    class="flex flex-col space-y-3 bg-gradient-to-br from-[#111729] to-[#1D1B48] text-[#CDD5E0] rounded-lg p-6"
  >
    <a :href="r.html_url" class="font-semibold text-xl hover:text-[#4A9DEC]">{{r.name}}</a>
    <p class="font-normal text-[#97A3B6]">
      {{r.description}}
    </p>
    <div class="flex flex-row items-center space-x-4 text-[#97A3B6]">
      <div  v-if="r.license" class="flex flex-row items-center space-x-2">
        <img src="../assets/resources/Chield_alt.svg" alt="" />
        <p>MIT</p>
      </div>
      <div class="flex flex-row items-center space-x-2">
        <img src="../assets/resources/Nesting.svg" alt="" />
        <p>{{r.forks}}</p>
      </div>
      <div class="flex flex-row items-center space-x-2">
        <img src="../assets/resources/Star.svg" alt="" />
        <p class="text-sm ml-2">{{ r.watchers }}</p>
      </div>
      <p class="text-sm ml-3">updated 4 days ago</p>
    </div>
  </div>
  
</template>
<script setup>
defineProps({
    repo: Array
})

</script>